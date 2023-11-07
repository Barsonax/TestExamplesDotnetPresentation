---
theme: white
transition: "slide"
highlightTheme: "vs2015"
slideNumber: true
#logoImg: "https://github.com/Barsonax/nukepresentation/raw/master/images/nukeIcon.png"
title: "Rock your tests!"
enableTitleFooter: false
customTheme : "my-theme"
---

## Rock your tests!

<a>
    <img style="border: unset; box-shadow: unset" data-src="https://github.com/Barsonax/nukepresentation/raw/master/images/nukeIcon.png">
</a>

---

## In deze presentatie

- Waarom testen?
- Wat is TestExamplesDotnet
- Hoe werkt TestExamplesDotnet
- Vragen

---

## Waarom (automatische) testen?

- Snelle feedback
- Bugs voorkomen
- Test driven design

--

## Test driven design

Tests kunnen design issues zichtbaar maken 

<span class="fragment">

```cs
context.Reservations.Add(new Reservation
{
    UserName = "",
    UserId = TestUser.NormalUser.Id
});
```

</span>

<span class="fragment"> Veel mocks? </span> <span class="fragment"> Verkeerde test scope </span> <span class="fragment"> of issue met de code? </span>

--

## Waarom TestExamplesDotnet?

- <span class="fragment">Testsuite met runtimes van > 1 uur</span>
- <span class="fragment">Flakyness</span>
- <span class="fragment">Welke functie testen we nou?</span>
- <span class="fragment">Dit kan beter</span>

--

## Unit/Integration testen

- Verschil niet zo belangrijk
- Snelheid is belangrijk
- Betrouwbaarheid is belangrijk
- Focus op wat testen we nou echt?

---

## Wat is TestExamplesDotnet?

- Een repository met efficiente test setups
- Geen handmatige setup
- Snelle feedback
- Echte database ipv een mock
- Core dev feedback loop

---

## Ingredienten

--

## WebApplicationFactory

- <https://learn.microsoft.com/en-us/aspnet/core/test/integration-tests?view=aspnetcore-7.0>
- Makkelijk je app draaien vanuit code
- In memory testserver
- Limitaties voor browser testen, daarover later meer

--

## Testcontainers?

- <https://dotnet.testcontainers.org/>
- Library om docker heen
- Handig voor dependencies zoals databases
- Zorgt voor cleanup, ook als je dit zelf vergeet

--

## Pooling

- Migraties zijn duur
- Hergebruik database is interessant
- Test isolatie mag niet gebroken worden

--

## Respawn

- <https://github.com/jbogard/Respawn>
- Ruimt database snel op
- Behoudt schema

--

## Lifecycle

<a>
    <img height=600em data-src="https://media.githubusercontent.com/media/Barsonax/TestExamplesDotnet/bf2ca7e4c629d884829c60a3f50a7434c7a66b79/Media/ApiTestsFlowChart.drawio.svg">
</a>

--

![](https://media.githubusercontent.com/media/Barsonax/TestExamplesDotnet/master/Media/2000testsin10sec.gif)

---

## En mijn frontend dan?

- Frontend mag geen blinde vlek zijn.
- Niet ootb mogelijk met WebApplicationFactory

--

## Playwright

- <https://playwright.dev/dotnet/>

---

## Vragen
