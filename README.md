# Beyond Compliance: Improving Cookie Consent Notice Comprehension and Usability Through Design Science Research

<img src="/repo-assets/dsr-ccn-optimized.png" width="400" alt="screenshot of the DSR Cookie Consent Notice"/>

This cookie consent notice accompanies **Beyond Compliance: Improving Cookie Consent Notice Comprehension and Usability Through Design Science Research**, published in [*Information and Computer Security*](https://www.emeraldgrouppublishing.com/journal/ics).


## Structured Abstract

### Purpose
Cookie consent notices frequently fail to communicate data practices clearly or support genuine privacy choices. This study aimed to improve user comprehension of website data practices and the usability of consent decisions in the South African context, where the Protection of Personal Information Act (POPIA) mandates informed consent for cookie-based data collection.

### Design/methodology/approach
Design Science Research (DSR) was employed across three iterative build-and-evaluate cycles. A typology of cookie consent notice designs was derived from the 100 most popular South African websites. The DSR artefact was refined through expert usability evaluation (*n*=5), a large-scale online experiment comparing comprehension and usability against the typology (*n*=320), and a between-subjects validation study (*n*=275). Twenty-three empirically, theoretically, and legally grounded design specifications guided development.

### Findings
Most existing South African cookie consent notices performed poorly on privacy comprehension and usability. The DSR artefact performed as well as or better than prevalent South African designs across most communication and usability measures, with statistically significant advantages on specific measures, though not uniformly across all iterations and outcomes. Labelled icons facilitated long-term retention of data practices, consistent with multimedia learning theory. However, third-party data sharing remained poorly understood regardless of notice design, suggesting terminology, not just visual design, may be a barrier worth testing directly in future work.

### Originality
This study provides the first empirical baseline for cookie consent communication and usability in South Africa, an open-source POPIA-compliant artefact, and 23 reusable design specifications. It extends multimedia learning theory to consent notice design and surfaces a possible boundary condition distinguishing structural from terminological comprehension barriers, motivating future work to test this distinction directly.

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

