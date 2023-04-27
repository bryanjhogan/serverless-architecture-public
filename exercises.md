The "product requirements" for these exercises are not fully fleshed out, make assumptions as you see fit and design an architecture to fit.

A large degree of hand waving, is fine. Connect this service to that, take its output and send it over there.

## 1. Podcast transcription 

On a regular basis check a podcast feed for new episodes. 

If there is a new episode, generate and store a transcript of the episode and notify users who are interested in the podcast. 

## 2. PDF text extraction

Allow the user to upload a document via an API, extract the text from the document (this will be asynchronous) and make the text available to the user when complete.

## 3. Document translation

Let the user upload a text file(s) via an API, specifying the source and destination languages. Translate the file, return the translation, and store the translation for later retrieval.

## 4. Object search

Upload photos for analysis. If the photos contain restricted objects, flag the photos. Generate a daily report based on what is found. 


## 5. Feedback form filter

MegaCorp with 200 departments has a single feedback form on its site. If the customer uses it correctly they select the product they are providing feedback on, but many don't. 

For feedback that doesn't have the product selected route the feedback to the correct department(s). 

## 6. Id check 

Design a system that checks if the person presenting the ID matches the image in the ID. 

## 7. Face as a ticket 

Instead of presenting a ticket, the person's face will grant them access to a location if they are registered. Entry and exit will be recorded. In the event of an emergency, message the people still in the location.

## 8. Check if a product is damaged 

Create a process that inspects if a product is damaged and notifies administrators if it is.  

## 9. Car park without tickets or keycard

Imagine a car park without entry/exit barriers and no tickets/passes. The users of the car park will be billed based on how long they are in the car park. Assume all car park users have a registered payment mechanism.

## 10. Interpreter 

Create an application that accepts text or speech, translates it to another language, and speaks the translation. 

## 11. Perform a scene from a play with different voices playing each part
 
Choose a scene from a play with a few characters. Using AI services, turn the text into audio. Store a record of the audio and make it available via HTTP.

## 12. Count the number of people in a location 

Some sports venues take photos of the whole audience, take in these photos, and count the number of people in the venue. Bonus points for de-duping faces.