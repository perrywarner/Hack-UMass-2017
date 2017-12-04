# Apotheca

> At Hack UMass 2017, our team had 48 hours to scramble together some project to "hack healthcare". You can see the result of our hackathon here.

## Table of Contents

- [Overview](#overview)
  - [Tools](#tools)
  - [Front-End](#front-end)
    - [Website](#website)
      - [Tree Structure of Website](#tree-structure-of-website)
      - [Core Components of the Website](#core-components-of-the-website)
        - [Pharma Search](#pharma-search)
        - [Symptom Search](#symptom-search)
        - [Dispenser Device Web UI](#dispenser-device-web-ui)
  - [Back End](#back-end)
    - [API](#api)
        - [Algolia](#algolia)
        - [Google Maps](#google-maps)

## Overview

Our project didn't win any awards, but we had an ambitious plan that had many parts successfully implemented. We created a web application with responsive UI that queries the user's current location and then finds pharmacies and doctors in a 25-mile radius. Additionally, we provide a feature so that common health symptoms are matched with over-the-counter drugs.

### Tools

- Used Google Firebase and JSON for storage of pharmaceutical information and medical symptoms (over the counter pharmaceuticals for legal reasons only): https://firebase.google.com/
- Implemented Google's slick new Material Design UI design framework: http://materializecss.com/
- Linked to the Google Maps API to allow the user to search for pharmacies, doctors and hospitals in a 25 mile radius: https://developers.google.com/maps/
- Used the Algolia Search API to query our JSON database for medicine that relieves symptoms: https://www.algolia.com/


[Back to Top](#table-of-contents)

### Front-End

#### Website

##### Tree Structure of Website

Here is a general overview on the structure of the site.

```json
Home page
	- Pharma Search
	- Symptom Search
```

[Back to Top](#table-of-contents)

##### Core Components of the Website

###### Pharma Search

- Uses Google Maps to find pharmacies in the local area that provide the medicine requested.

###### Symptom Search

- Uses Algolia to search our database for medicine that will help relieve symptoms a user is suffering from in order of relevance.

[Back to Top](#table-of-contents)

### Back End

#### API

###### Algolia

- Queries database for medicine that relieves symptoms.

###### Google Maps

- Show locations of pharmacies and general stores where medicine may be purchased to relieve symptoms.

[Back to Top](#table-of-contents)

### Hardware

[Back to Top](#table-of-contents)
