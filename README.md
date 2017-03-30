# Zucchini for Liferay

Zucchini extension for Liferay Projects

## Usage

```xml
<dependency>
    <groupId>br.com.entelgy</groupId>
    <artifactId>zucchini-liferay</artifactId>
    <version>1.0.0</version>
    <scope>test</scope>
</dependency>

```
### Configuration

[https://entelgy-brasil.github.io/zucchini/](https://entelgy-brasil.github.io/zucchini/)

### Example

```cucumber
#language: en
@it
Feature: Navigate to public home

Scenario:  Navigate to public home with a loged USer
  Given user "test@liferay.com" is logged in liferay
    Then I navigate to "web/guest/home"
    Then element having id "portlet-id" should be present
    Then logout in liferay
```

## Steps

### Liferay Steps

* Given user "{email}" is logged in liferay
* Then login as "{email}" in liferay
* Then go to control panel
* Then go to "{uri}"
* Then logout in liferay
* Then I navigate to preferences of portlet "{[contains(@id)}"
* Then I come back to portlet