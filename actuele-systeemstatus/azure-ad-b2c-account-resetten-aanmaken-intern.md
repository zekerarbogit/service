---
if: visitor.claims.unsigned.isArboUser
---

# Azure AD B2C account resetten/aanmaken (Intern)

{% @supademo/embed demoId="cmk71abjw00bow60ih5b7zwzc" url="https://app.supademo.com/demo/cmk71abjw00bow60ih5b7zwzc" fullWidth="true" %}

Voor wie is dit artikel? Alleen voor medewerkers die toegang hebben tot Azure AD.

#### **Wanneer gebruik je dit? Volg dit stappenplan in twee situaties:**

1. Account niet gevonden: Een klantgebruiker (werkgever/medewerker) staat wel in Planningsagenda, maar krijgt de melding dat het account niet gevonden kan worden bij het inloggen.
2. Geen toegang meer tot 2FA methode (authenticator app, telefoon): De gebruiker heeft geen toegang meer tot en kan dit zelf niet herstellen.

Je controleert hiermee of het account bestaat in Azure AD B2C. Zo niet, dan maak je het aan. Bestaat het wel, dan verwijder je het en maak je het opnieuw aan om de inlogproblemen op te lossen.

## **Stappenplan**

{% stepper %}
{% step %}
#### Inloggen Azure Portal&#x20;

Ga naar [portal.azure.com/portalzvdzsso.onmicrosoft.com](https://portal.azure.com/portalzvdzsso.onmicrosoft.com) en log in met je beheerdersaccount.
{% endstep %}

{% step %}
#### Navigeer naar Users

* Open onder 'Azure services' de optie **Microsoft Entra ID.**
* Klik in het linkermenu onder 'Manage' op **Users**.
{% endstep %}

{% step %}
#### Zoek de gebruiker

* Klik op _'Want to switch back to the legacy users list experience? Click here to switch'_ om makkelijker te zoeken.
* Zoek op het e-mailadres of de naam (display name) van de gebruiker.
{% endstep %}

{% step %}
#### Bestaat het account?

* **Ja:** Account verwijderen
  * Open de gebruiker en controleer goed of je de juiste persoon hebt.
    * Klik op **Delete** om de gebruiker uit B2C te verwijderen.
    * Klik nogmaals op **Delete** om de verwijdering definitief te maken.
    * Ga terug naar de gebruikerslijst en klik op **Refresh** om de lijst bij te werken.
* **Nee:** Ga door naar volgende stap.&#x20;
{% endstep %}

{% step %}
#### Nieuw account aanmaken

* Klik in de gebruikerslijst op **New User.**
* Selecteer **Create** **new user**.
* Kies bij 'Choose a method' voor **Email**.
* Vul het e-mailadres van de gebruiker in.
* Vul de volledige naam in bij het veld 'Name'.
* Klik op **Create** om het account aan te maken.
{% endstep %}

{% step %}
#### Afronden&#x20;

Laat de gebruiker opnieuw inloggen op het portaal. Het account is nu gereset en de gebruiker kan het instelproces (wachtwoord en 2FA) opnieuw doorlopen.
{% endstep %}

{% step %}
#### Mail versturen

**Als je account gereset hebt stuur dan deze mail.**&#x20;

```
Onderwerp: Account voor het Werkgeversportaal van ZekerArbo opnieuw ingesteld
Beste klant.
 
Omdat je geen toegang (meer) had tot je 2FA middel (bijvoorbeeld een oud telefoonnummer), hebben we je account opnieuw ingesteld. Om weer toegang te krijgen tot je account, moet je eerst je wachtwoord wijzigen. Dit doe je als volgt:
1.	Ga naar portaal.zekerarbo.nl en voer je e-mailadres is en klik op Volgende
2.	Op het volgende scherm kun je kiezen voor de optie “Wachtwoord vergeten”. Via deze link kun je een nieuw wachtwoord instellen.
 
Je account optimaal beveiligen
Je 2FA-methode is nu teruggezet op e-mail. We raden aan om deze aan te passen naar SMS of Authenticator app. Nadat je het wachtwoord hebt gewijzigd, kun je de 2FA-methode aanpassen via deze link.
 
Met vriendelijke groet,
ZekerArbo
 

```

**Account bestond nog niet mail**

```
Onderwerp: Inloggen in het Werkgeversportaal van ZekerArbo
Beste klant.
 
We hebben je account opnieuw ingesteld. Om toegang te krijgen tot je account, moet je eerst je wachtwoord wijzigen. Dit doe je als volgt:
1.	Ga naar portaal.zekerarbo.nl en voer je e-mailadres is en klik op Volgende.
2.	Op het volgende scherm kun je kiezen voor de optie “Wachtwoord vergeten”. Via deze link kun je een nieuw wachtwoord instellen.
 
Je account optimaal beveiligen
Je 2FA-methode staat nu op e-mail. We raden aan om deze aan te passen naar SMS of Authenticator app. Nadat je het wachtwoord hebt gewijzigd, kun je de 2FA-methode aanpassen via deze link.
 
Met vriendelijke groet,
ZekerArbo
 

```
{% endstep %}
{% endstepper %}
