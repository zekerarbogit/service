---
hidden: true
---

# Werkwijze problemen inloggen

Deze workflow beschrijft de stappen bij problemen met inloggen in het portaal.

{% stepper %}
{% step %}
### Klantmelding

De klant belt of mailt met een vraag of probleem over het portaal.
{% endstep %}

{% step %}
### Gegevens uitvragen

Vraag met welk e-mailadres de klant probeert in te loggen en doe een verificatie om de identiteit van de klant te controleren.&#x20;

{% hint style="warning" %}
[Lees hier wat de juiste werkwijze is](werkwijze-klant-verifieren.md)
{% endhint %}
{% endstep %}

{% step %}
### Account opzoeken

Ga naar **Planningsagenda → Klant gebruikers**.

Zoek het account op via het e-mailadres.
{% endstep %}

{% step %}
### Bestaat het account?

* **Ja** → ga door bij [Account bestaat](werkwijze-problemen-inloggen.md#account-bestaat).
* **Nee** → ga door bij [Account niet gevonden](werkwijze-problemen-inloggen.md#account-niet-gevonden).
{% endstep %}
{% endstepper %}

## Account bestaat

{% stepper %}
{% step %}
### Rol controleren

Open de opgezochte gebruiker en bekijk welke rol deze heeft.&#x20;

Staat de rol op **Migratie**? Pas deze aan naar rol **1, 2, 3 of 4** via **Bewerken**.

{% hint style="danger" %}
**1 WG - Geen koppeling met systeem WG - Inzage op organisatieniveau - ZekerArbo**

Dit is de administrator/werkgeversrol, deze mag niet zomaar toegekend worden aangezien het inzage geeft in alle medewerkers van het bedrijf en de rechten kan bepalen van alle HR medewerkers.&#x20;

_Deze rol kan ook niet toegekend worden wanneer er een koppeling is met verzuim/HR systeem van de klant._
{% endhint %}

{% hint style="warning" %}
**2 LG - Geen koppeling met systeem WG - Inzage eigen afdeling -ZekerArbo**

Dit is de rol voor meeste HR medewerkers, de werkgever/administrator moet de juiste rechten toekennen om medewerkers te kunnen zien. Geen beheer van rechten collega's.&#x20;

_Deze rol kan ook niet toegekend worden wanneer er een koppeling is met verzuim/HR systeem van de klant._
{% endhint %}

{% hint style="danger" %}
**3 WG - Ziekmelding via koppeling met systeem WG - Inzage op organisatieniveau - ZekerArbo**

Dit is de administrator/werkgeversrol, deze mag niet zomaar toegekend worden aangezien het inzage geeft in alle medewerkers van het bedrijf en de rechten kan bepalen van alle HR medewerkers.&#x20;

_Deze rol kan alleen worden toegekend wanneer er een koppeling is met verzuim/HR systeem van de klant._


{% endhint %}

{% hint style="warning" %}
**4 LG - Ziekmelding via koppeling met systeem WG - Inzage op eigen afdeling - ZekerArbo**

Dit is de rol voor meeste HR medewerkers, de werkgever/administrator moet de juiste rechten toekennen om medewerkers te kunnen zien. Geen beheer van rechten collega's.&#x20;

_Deze rol kan alleen worden toegekend wanneer er een koppeling is met verzuim/HR systeem van de klant._
{% endhint %}
{% endstep %}

{% step %}
### E-mailadres controleren

Open het account en kies **Bewerken**.

Controleer of het e-mailadres op **alle 4 plekken** correct staat ingevuld.

**Velden**

* Email
* Gebruikersnaam
* SSO ZekerArbo B2C Klanten
* SSO ZekerArbo Intern
{% endstep %}

{% step %}
### Eerder ingelogd?

Ga terug naar **Planningsagenda → Klant gebruikers**.

Kijk naar **Laatste inlog**. Is de klant eerder ingelogd?&#x20;

* **Nee** → laat de klant via [**Wachtwoord vergeten**](https://app.gitbook.com/s/hkUne0pNVHithYNGENV4/werkgevers/inloggen/wachtwoord-opnieuw-instellen) een wachtwoord instellen.
* **Ja** → laat de klant opnieuw proberen in te loggen.
{% endstep %}

{% step %}
### Nog steeds foutmelding?

Als de fout blijft: controleer of het account is doorgeschoten naar **B2C**.

Ga door bij [B2C controle](werkwijze-problemen-inloggen.md#b2c-controle).
{% endstep %}
{% endstepper %}

## B2C controle

{% stepper %}
{% step %}
### B2C status bepalen

[Niet elke medewerker kan dit controleren, vraag dit na bij je leidinggevende. ](#user-content-fn-1)[^1]



* **Niet doorgeschoten** → voer het account op bij **B2C**.
* **Wel doorgeschoten** → verwijder het account volledig en voer het opnieuw in.

{% hint style="warning" %}
Verwijderen en opnieuw opvoeren is ingrijpend. Doe dit alleen als het account al in B2C staat en de login blijft falen.
{% endhint %}
{% endstep %}
{% endstepper %}

### Account niet gevonden

{% stepper %}
{% step %}
### Inactieve gebruikers controleren

Controleer onder **Inactieve gebruikers**. (In Planningsagenda: Klant Gebruikers → tab inactieve gebruikers

* **Account gevonden** → maak actief, stel juiste rol in, en ga verder bij [Account bestaat](werkwijze-problemen-inloggen.md#account-bestaat).
{% endstep %}

{% step %}
### Zoeken op bedrijfsnaam

Is er geen account te vinden op e-mailadres én niet bij inactieve gebruikers?

Zoek dan op **bedrijfsnaam**.
{% endstep %}

{% step %}
### Ander account gevonden

Geef aan dat de gebruiker zelf een account moet aanmaken via **service.zekerarbo.nl**.
{% endstep %}

{% step %}
### 13. Geen account gevonden

Vraag het e-mailadres opnieuw.

Controleer bij **Bedrijven** of het e-mailadres als **contactpersoon** staat genoteerd.
{% endstep %}
{% endstepper %}

[^1]: fdsdsfds
