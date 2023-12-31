# dsr-cookie-consent-notice

<img src="/repo-assets/dsr-ccn-optimized.png" width="400" alt="screenshot of the DSR Cookie Consent Notice"/>

This cookie consent notice is the final arfact for my UCT Masters of Commerce in Information Systems research project. The research utilized a [Design Science Research (DSR)](http://www.desrist.org/desrist/content/design-science-research-in-information-systems.pdf) methodolgy and aimed to improve cookie consent notice communication and usability. This artefact was compared to a typology of seven prominent cookie consent notice types observed on the 100 most popular South Africa websites. Three design and build cycles took place, each followed by an evaluation. The evaluations were in the form of online experiments, and tested privacy communication and usability.

### Abstract
Cookie consent notices have become increasingly popular worldwide, especially since the introduction of the GDPR. Their purpose is to gain consent for data collection and processing (including tracking) from website users. However, privacy notices and controls are ineffective at informing end-users. Furthermore, they often hinder users from expressing their privacy choices. Research has shown that most individuals appear not to be empowered to practice their rights to online privacy and lawful consenting. There are substantial ethical, legal and commercial reasons to improve cookie consent notices so that privacy policies are understood, consent is informed, and individuals have the power to choose whether and how personal information is collected and processed. Alongside the dissertation, a working instantiation of a cookie consent notice comprised of deployable code and graphical interface components was developed as a possible solution. A Design Science Research (DSR) approach was used. The DSR artefact was compared to a selection of prevalent cookie consent notice types used in South Africa. Three evaluation rounds took place, focused on usability and communication. The final artefact exists in this open-source code repository for practitioners to use, develop and extend.

Initial code adapted from [GlowCookies](https://github.com/manucaralmo/GlowCookies) by Almoguera (2021).

### Demo
View the demo [here](https://happyhols.co.za/h/)

### CSS
The cookie consent notice makes use of [Bulma](https://bulma.io/), a free, open source CSS framework. However, this can easily be replaced if you prefer to use your own CSS.

### How to use this cookie consent notice
Insert this code in your html `<head>` tag.
```html
<!--Import Bulma CSS -->
<link rel="stylesheet" href="bulma.min.css">

<!-- JavaScript for DSR Cookie Consent Notice-->
<script src="dsr-ccn.js"></script> 
<script>
    cookieConsentNotice.start('en', {
        analytics: 'G-8PDMD2MD95', 
        hideAfterClick: false,
        showDataCollectedDeviceDetails: true,
        showDataCollectedIdentifiers: true,
        showDataCollectedBrowsingHistory: true,
        showDataCollectedLocation: true,
        showDataSharedDeviceDetails: true,
        showDataSharedIdentifiers: true,
        showDataSharedBrowsingHistory: true,
        showDataSharedLocation: true,
        border: 'none',
        position: 'left',
        policyLink: 'https://yourdomain.co.za/privacy-policy/',
        bannerDescription: 'Do you consent to the use of third-party cookies as described below? Read more in our',
        bannerLinkText: 'Privacy Policy.',
        bannerBackground: '#ffffff',
        acceptBtnText: 'Accept',
        acceptBtnBorder: 'none',
        acceptBtnBackground: '#ECF7FE',
        rejectBtnText: 'Decline',
        rejectBtnBorder: 'none',
        rejectBtnBackground: '#0B67A5',
        manageColor: '#ffffff',
        manageBackground: '#0B67A5' 
      });
</script>
```
Note, most options are configurable. Simply set the options to true/false, or add a custom string or hex code colour where required.


## Tracking options
These are the parameters that you can modify to add your tracking codes or custom scripts.

| Parameter               | Type   | Values                                                                                                              |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------------------------- |
| `analytics`             | String | Example: `"G-8PDMD2MD95"` (Analytics tracking code)                                                                 |
| `facebookPixel`         | String | Example: `"990955817632222"` (Facebook Pixel code)                                                                  |
| `HotjarTrackingCode`    | String | Example: `"990955817632322"` (Hotjar tracking code)                                                                 |
| `customScript` (inline) | Object | Example: `[{ type: 'custom', position: 'body', content: 'console.log('custom script');' }]`                         |
| `customScript` (src)    | Object | Example: `[{ type: 'src', position: 'head', content: 'https://www.googletagmanager.com/gtag/js?id=G-FH87DE17XF' }]` |


### References:
Almoguera, M. C. (2021). GlowCookies (Version 3.1.6) [Computer source code]. GitHub. https://github.com/manucaralmo/GlowCookies

