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

#### **Stappenplan**

{% stepper %}
{% step %}
#### Inloggen Azure Portal&#x20;

Ga naar [portal.azure.com/portalzvdzsso.onmicrosoft.com](https://portal.azure.com/portalzvdzsso.onmicrosoft.com) en log in met je beheerdersaccount.
{% endstep %}

{% step %}
#### Navigeer naar Users

* Open onder 'Azure services' de optie Microsoft Entra ID.
* Klik in het linkermenu onder 'Manage' op Users.
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
    * Klik op Delete om de gebruiker uit B2C te verwijderen.
    * Klik nogmaals op Delete om de verwijdering definitief te maken.
    * Ga terug naar de gebruikerslijst en klik op Refresh om de lijst bij te werken.
* **Nee:** Ga door naar volgende stap.&#x20;
{% endstep %}

{% step %}
#### Nieuw account aanmaken

* Klik in de gebruikerslijst op New User.
* Selecteer Create new user.
* Kies bij 'Choose a method' voor Email.
* Vul het e-mailadres van de gebruiker in.
* Vul de volledige naam in bij het veld 'Name'.
* Klik op 'Create' om het account aan te maken.
{% endstep %}

{% step %}
#### Afronden&#x20;

Laat de gebruiker opnieuw inloggen op het portaal. Het account is nu gereset en de gebruiker kan het instelproces (wachtwoord en 2FA) opnieuw doorlopen.

Hiervoor ontvangen ze instructies via de mail.&#x20;
{% endstep %}
{% endstepper %}
