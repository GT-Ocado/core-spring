<img src="https://github.com/stayahead-training/shared/blob/master/stayahead.png" />

# IoC and DI Assignment

## Currency Converter (Java Config)

[<< back](../../../../README.md#ioc-and-di)

You're going to Springify a currency converter app. That is, you're going to have Spring instantiate and manage beans whose function it is to convert a monetry value from one currency to another. In this version, you're going to configure the bean container using a Java class.

[Download this project](spring-essentials_assignments_ioc-and-di_currency-converter-java-config.zip) to get started. 

The CurrencyConverter class looks like this:

```java
public class CurrencyConverter {

  private Currency baseCurrency;
  private Map<CurrencyPair, BigDecimal> exchangeRates;

  public CurrencyConverter(Currency baseCurrency) {
    this.baseCurrency = baseCurrency;
    exchangeRates = new HashMap<>();
    exchangeRates.put(new CurrencyPair(GBP, EUR), BigDecimal.valueOf(1.18));
    exchangeRates.put(new CurrencyPair(GBP, USD), BigDecimal.valueOf(1.31));
    exchangeRates.put(new CurrencyPair(GBP, GBP), BigDecimal.valueOf(1));
    exchangeRates.put(new CurrencyPair(EUR, GBP), BigDecimal.valueOf(0.85));
    exchangeRates.put(new CurrencyPair(EUR, USD), BigDecimal.valueOf(1.11));
    exchangeRates.put(new CurrencyPair(EUR, EUR), BigDecimal.valueOf(1));
    exchangeRates.put(new CurrencyPair(USD, GBP), BigDecimal.valueOf(0.76));
    exchangeRates.put(new CurrencyPair(USD, EUR), BigDecimal.valueOf(0.90));
    exchangeRates.put(new CurrencyPair(USD, USD), BigDecimal.valueOf(1));
  }

  public BigDecimal convert(BigDecimal amount, Currency otherCurrency) {
    return amount.multiply(exchangeRates.get(new CurrencyPair(baseCurrency, otherCurrency)));
  }
}
```

The constructor accepts a base currency - the currency from which to convert. The convert method accepts an amount and another currency, and returns the converted amount.

The executable App class looks like this:

```java
public class App {

  public static void main(String[] args) {
    Currency baseCurrency = GBP;
    CurrencyConverter cc = new CurrencyConverter(baseCurrency);
    System.out.printf("100.00%s is worth %sGBP\n", baseCurrency, cc.convert(BigDecimal.valueOf(100), GBP));
    System.out.printf("100.00%s is worth %sEUR\n", baseCurrency, cc.convert(BigDecimal.valueOf(100), EUR));
    System.out.printf("100.00%s is worth %sUSD\n", baseCurrency, cc.convert(BigDecimal.valueOf(100), USD));
  }
}
```
### Part 1

1. Add to the POM the `spring-context` dependency.

2. Add a class to the main package named `AppContextConfig` and in it configure a CurrencyConverter bean with a base currency of GBP.<details>
    <summary>Show me</summary>

    ```java
    public class AppContextConfig {

      @Bean
      public CurrencyConverter currencyConverter() {
        return new CurrencyConverter(Currency.GBP);
      }
    }
    ```
</details>

3. In App::main instantiate a bean container referencing your bean config class.<details>
    <summary>Show me</summary>

    ```java
    ApplicationContext context = new AnnotationConfigApplicationContext(AppContextConfig.class);
    ```
</details>

4. In App::main obtain a reference to the CurrencyConverter bean from the bean container instead of instantiating it directy.<details>
    <summary>Show me</summary>

    ```java
    CurrencyConverter cc = context.getBean(CurrencyConverter.class);
    ```
</details>

5. Run it!

### Part 2

Let's extract the obtaining of the exchange rate into a separate bean.

1. Add a class to the beans package named `ExchangeRateService` with a method named `getExchangeRate` that accepts two currencies and returns an exchange rate. Note that this will involve moving some code from the CurrencyConverter class.<details>
	<summary>Show me</summary>

	```java
	public class ExchangeRateService {

 	  private Map<CurrencyPair, BigDecimal> exchangeRates;

	  public ExchangeRateService() {
	    exchangeRates = new HashMap<>();
	    exchangeRates.put(new CurrencyPair(GBP, EUR), BigDecimal.valueOf(1.18));
	    exchangeRates.put(new CurrencyPair(GBP, USD), BigDecimal.valueOf(1.31));
	    exchangeRates.put(new CurrencyPair(GBP, GBP), BigDecimal.valueOf(1));
	    exchangeRates.put(new CurrencyPair(EUR, GBP), BigDecimal.valueOf(0.85));
	    exchangeRates.put(new CurrencyPair(EUR, USD), BigDecimal.valueOf(1.11));
	    exchangeRates.put(new CurrencyPair(EUR, EUR), BigDecimal.valueOf(1));
	    exchangeRates.put(new CurrencyPair(USD, GBP), BigDecimal.valueOf(0.76));
	    exchangeRates.put(new CurrencyPair(USD, EUR), BigDecimal.valueOf(0.90));
	    exchangeRates.put(new CurrencyPair(USD, USD), BigDecimal.valueOf(1));
	  }
		
	  public BigDecimal getExchangeRate(Currency from, Currency to) {
	    return exchangeRates.get(new CurrencyPair(from, to));
	  }
	}
	```
</details>

2. Modify the CurrencyConverter class such that it uses an ExchangeRateService instance to perform the conversion. Note that the ExchangeRateService should be autowired.<details>
	<summary>Show me</summary>

	```java
	public class CurrencyConverter {

	  private Currency baseCurrency;

	  @Autowired
	  private ExchangeRateService exchangeRateService;

	  public CurrencyConverter(Currency baseCurrency, ExchangeRateService exchangeRateService) {
	    this.baseCurrency = baseCurrency;
	    this.exchangeRateService = exchangeRateService;
	  }

	  public BigDecimal convert(BigDecimal amount, Currency otherCurrency) {
	    return amount.multiply(exchangeRateService.getExchangeRate(baseCurrency, otherCurrency));
	  }
	}
	```
</details>

3. In AppContextConfig configure an ExchangeRateService bean.<details>
	<summary>Show me</summary>

	```java
	@Bean
	public ExchangeRateService exchangeRateService() {
	  return new ExchangeRateService();
	}
	```
</details>

4. Run it!

[<< back](../../../../README.md#ioc-and-di)
