# IoC and DI Assignment

## Currency Converter (Component Scanning and Properties)

[<< back](../../../#2-ioc-and-di)

You're going to Springify a currency converter app. That is, you're going to have Spring instantiate and manage beans whose function it is to convert a monetry value from one currency to another. In this version, you're going to configure the bean container using component scanning and a properties file.

Clone this repo to get started: 
https://github.com/stubailey18/stayahead.spring_essentials.ioc_and_di.currency_converter_comp_scan_and_props.git

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

TODO

[<< back](../../../#2-ioc-and-di)
