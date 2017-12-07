# Apotheca

At Hack UMass 2017, our team had 48 hours to scramble together some project to "hack healthcare". Our project didn't win any awards, but we had an ambitious plan that had many parts successfully implemented. We created a web application with responsive UI that queries the user's current location and then finds pharmacies and doctors in a 25-mile radius. Additionally, we provide a feature so that common health symptoms are matched with over-the-counter drugs.

We originally intended for our project to be related to an **Automated Pill Dispenser** built with a Raspberry Pi, Node.js, and an MQTT framework - but this was a bit too much for us to digest. The project you see now is what was turned in at the end. 

## Getting Started

You can see a static version of our website at http://apotheca.s3-website.us-east-2.amazonaws.com/ . Because this is a static version of the website, our Google Maps API and Algolia API are currently broken. However, if you get the whole site running locally, you will be able to see the Google Maps API get your current location and find you a pharmacy.

[Back to Top](#Apotheca)

## Steps to get Started

Our index.html file is located under _Hack-UMass-2017/src/public/index.html_. You can view our project working by simply opening index.html, provided you fulfill the following requirements: 
- You must have an internet connection so the Google Maps API and Algolia can connect.
- You must have cloned the repository to your local machine. If you're unsure about how to do this, check out https://help.github.com/articles/cloning-a-repository/ 
- We haven't tested our project with any web browser than Google Chrome. YMMV with Edge, IE, Firefox, ect.

Otherwise, if you want to check out the code, you will find that we have a very front-end heavy project:
- Most of our work was done on the various HTML files, which are found at _/src/public_.
- We link to Algolia with the Javascript files, which are primarily located within _/src/public/js_ .
- You will find within _/src/public/js_ and _/src/public/css_ very large files, corresponding with Materialize, our CSS framework - we, of course, didn't make these. To those that are interested, Materialize is very similar in terms of implementation to [Twitter's Bootstrap](https://getbootstrap.com/)
- The JSON files within _/src_ are metadata options for Google Firebase, and you won't have access to these things without the Google Firebase login. As a side note, there is the Google Maps API key listed in there - this is very insecure, and it should be deleted..

[Back to Top](#Apotheca)

## Built With

* [Materialize](http://materializecss.com/) - "A modern responsive front-end framework based on Material Design (by Google)". Materialize is the UI toolkit mentioned above, and provides a nice alternative to the popular Twitter's Bootstrap.
* [Google Firebase](https://firebase.google.com/) - Used Google Firebase and JSON for storage of pharmaceutical information and medical symptoms (over the counter pharmaceuticals for legal reasons only). Unfortunately, if you build our project, you won't see anything of the sort working live - this is due to the fact that currently (as of Wednesday, Dec 6, 2017) our Algolia API key is invalid.
* [Algolia Search](https://www.algolia.com/) - Used the Algolia Search API to query our JSON database for medicine that relieves symptoms, as mentioned above. 
* [Google Maps API](https://developers.google.com/maps/) - Linked to the Google Maps API to allow the user to search for pharmacies, doctors and hospitals in a 25 mile radius. There are a few issues related to this API, and one glaring issue is that the location finder for Hospitals is hard-coded to UMass Amherst only, as opposed to taking the user's current location.

[Back to Top](#Apotheca)

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us. 

- We are very graciously stealing that writeup for our own project. Thank you!

[Back to Top](#Apotheca)

## Authors

* **Kathy Starr-Mitchell** - *Researched Raspberry Pi and MQTT technologies, and added "find local pharmacies" feature to Google Maps API* - [kstarrmitche](https://github.com/kstarrmitche)
* **Amanda Morrison** - *Added much for the front-end UI of Apotheca, including symptom-finder popup, symptom-finder form, contact list, and more* - [amorrison61689](https://github.com/perrywarner/Hack-UMass-2017/commits?author=amorrison61689)
* **Perry Warner** - *Researched MaterializeCSS and Google Maps API technologies, and added generic "find x in 25 mile radius" feature for Google Maps*
* **Zakar Handricken** - *Researched and provided all of the functionality that was completed for Google Firebase and Algolia Search*

See also the list of [contributors](https://github.com/perrywarner/Hack-UMass-2017/graphs/contributors) who participated in this project.

[Back to Top](#Apotheca)

## License

This project is licensed under the MIT License.

[Back to Top](#Apotheca)

## Acknowledgments

* Great job to Kathy for doing so much with Raspberry Pi and MQTT! Ultimately, this feature was a bit too ambitious for a two-day hackathon, as an Automated Pill Dispenser is something that could take months. We apologize that this Github Repository doesn't reflect just how much time and effort you put into this.
* Good job to Amanda Morrison for writing a lot of code that ended up in the final version, given that she is still currently taking only the third computer science class: Data Structures!

[Back to Top](#Apotheca)

