---
if: visitor.claims.unsigned.isArboUser
---

# Werkwijze problemen inloggen - Klantgebruiker (werkgever/leidinggevende)

Deze handleiding is onderdeel van 'First Time Fix'. ZekerArbo heeft als doel de klant in één keer te kunnen gaan helpen, door meer rechten en mogelijkheden te geven om een probleem direct op te lossen.&#x20;

Deze workflow beschrijft de stappen bij problemen met inloggen in het portaal of problemen met zichtbaarheid van documenten.

{% stepper %}
{% step %}
### Klantmelding

De klant belt of mailt met een vraag of probleem over inloggen op het (werkgevers) klantportaal.&#x20;
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

* **Ja** → ga door bij [Account bestaat](werkwijze-problemen-inloggen-klantgebruiker-werkgever-leidinggevende.md#account-bestaat-controle-gegevens).
* **Nee** → ga door bij [Account niet gevonden](werkwijze-problemen-inloggen-klantgebruiker-werkgever-leidinggevende.md#account-niet-gevonden).
{% endstep %}
{% endstepper %}

## Account bestaat - Controle gegevens

{% stepper %}
{% step %}
### Standaard vragen

Om welk probleem gaat het?&#x20;

* **Wachtwoord werkt niet →** ga door naar volgende stap
* **2FA werkt niet →** ga door naar [2FA problemen](werkwijze-problemen-inloggen-klantgebruiker-werkgever-leidinggevende.md#id-2fa-problemen)
* **Geen medewerkers zichtbaar →** ga door naar [#geen-medewerkers-zichtbaar](werkwijze-problemen-inloggen-klantgebruiker-werkgever-leidinggevende.md#geen-medewerkers-zichtbaar "mention")
{% endstep %}

{% step %}
### Gebruiker openen

Open de opgezochte gebruiker in Planningsagenda door erop te klikken, kies vervolgens **Bewerken**.
{% endstep %}

{% step %}
### Rol controleren

Staat de rol op **Migratie**? Pas deze aan naar rol **1, 2, 3 of 4**.

Bekijk of er andere gebruikers zijn in Planningsagenda bij hetzelfde bedrijf.&#x20;

Staan daar WG rollen tussen? Ken dan een LG rol toe. Geef aan dat de authorisaties en rollen door een collega aangepast kunnen worden.&#x20;



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

**Controleer in Planningsagenda de gegevens van de gebruiker.**

1. **Controleer op leestekens** (`&amp;`) Kijk of er `&amp;` in het e-mailadres staat.
   * **Ja**: Haal `amp;` weg en laat alleen `&` staan.
2. **Controleer de 3 velden** Zorg dat het correcte e-mailadres op alle drie de plekken identiek staat ingevuld:
   * Email
   * Gebruikersnaam
   * SSO ZekerArbo B2C Klanten

Wat is de vervolgstap?

**Heb je `&amp;` verwijderd uit het e-mailadres?** &#x20;

* **Ja** → Ga direct door naar het onderdeel [#id-2fa-reset-and-account-herstel-azure-a-d-b2c](werkwijze-problemen-inloggen-klantgebruiker-werkgever-leidinggevende.md#id-2fa-reset-and-account-herstel-azure-a-d-b2c "mention")
* **Nee**→  (het adres stond al goed): Ga verder met de stappen hieronder.
{% endstep %}

{% step %}
### Eerder ingelogd?

Ga terug naar **Planningsagenda → Klant gebruikers**.

Kijk naar **Laatste inlog**. Is de klant eerder ingelogd?&#x20;

* **Nee** → laat de klant via [**Wachtwoord vergeten**](https://app.gitbook.com/s/hkUne0pNVHithYNGENV4/werkgevers/inloggen/wachtwoord-opnieuw-instellen) een wachtwoord instellen en test dit direct.
* **Ja** → laat de klant opnieuw proberen in te loggen, wacht totdat dit is gelukt.
{% endstep %}

{% step %}
### Nog steeds foutmelding?

Als de fout blijft: controleer of het account is doorgeschoten naar **B2C**.

Ga door bij [#id-2fa-reset-and-account-herstel-azure-a-d-b2c](werkwijze-problemen-inloggen-klantgebruiker-werkgever-leidinggevende.md#id-2fa-reset-and-account-herstel-azure-a-d-b2c "mention")
{% endstep %}
{% endstepper %}

## 2FA Reset & Account Herstel - Azure AD B2C

Wanneer alle bovenstaande stappen zijn doorlopen en het account goed staat in planningsagenda kun je dit proces doorlopen

**Gebruik dit stappenplan in twee situaties:**

1. **2FA Problemen**: De gebruiker heeft 2FA ingesteld (App of SMS) maar heeft hier geen toegang meer toe. De enige oplossing is een volledige reset in Azure AD B2C.
2. **Inlogfouten**: De gebruiker krijgt de melding "Account niet gevonden" of blijft in een loop hangen.

Wie mag dit uitvoeren? Alleen onderstaande medewerkers hebben toegang om deze reset uit te voeren:

{% hint style="warning" %}
**De volgende medewerkers kunnen dit voor je oplossen:**

Bjorn Koeman

Patricia Langhorst

Inge Floor

Tamara Baars
{% endhint %}

[azure-ad-b2c-account-resetten-aanmaken-intern.md](azure-ad-b2c-account-resetten-aanmaken-intern.md "mention")



## Account niet gevonden

{% stepper %}
{% step %}
### Inactieve gebruikers controleren

Controleer onder **Inactieve gebruikers**. (In Planningsagenda: **Klant Gebruikers** → tab **inactieve gebruikers**

* **Account gevonden** → ga verder bij [Account bestaat](werkwijze-problemen-inloggen-klantgebruiker-werkgever-leidinggevende.md#account-bestaat) (hier pas je de rol aan).
{% endstep %}

{% step %}
### Zoeken op bedrijfsnaam

Is er geen account te vinden op e-mailadres én niet bij inactieve gebruikers?

Zoek dan op **bedrijfsnaam**.
{% endstep %}

{% step %}
### Ander account gevonden onder bedrijfsnaam

Geef aan dat de werkgever zelf een account moet aanmaken. Geef deze instructies door:[Aanmaken account voor leidinggevende](https://app.gitbook.com/s/hkUne0pNVHithYNGENV4/werkgevers/gebruik-portaal/aanmaken-account-voor-leidinggevende "mention")
{% endstep %}

{% step %}
### Geen klantgebruiker gevonden wel bedrijf

Vraag het e-mailadres opnieuw.

Controleer bij **Bedrijven** of het e-mailadres als **contactpersoon** staat genoteerd.\
Als dit niet zo is dan moet er een admin klantgebruiker aangemaakt worden.&#x20;

Voordat je dit doet is een uitgebreide verificatie belangrijk.


{% endstep %}
{% endstepper %}

## Geen medewerkers zichtbaar

Er kunnen meerdere redenen zijn dat er geen medewerkers zichtbaar zien.&#x20;

1. Klant heeft een LG gebruikersrol en heeft nog geen afdelingen/cliënten toegekend in de authorisatie.&#x20;
2. Bij het bedrijf bestaat er geen werkgeversrol, dus de authorisaties kunnen niet door de klant worden ingesteld.
