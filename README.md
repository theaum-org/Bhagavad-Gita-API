## Introduction

[TheAum.org](https://theaum.org/) presents a **free**, **anonymous** and highly available API for the Bhagavad Gita. 

[https://bhagavadgita.theaum.org/](https://bhagavadgita.theaum.org/)

## Motivation

Many existing APIs of the Gita requires you to either sign-up or get some token to perform requests. 
We feel like this is not something one wants when reading The Gita. 
Holy books and texts should be generally available and not holding any string attached to it, therefore we created this completely free and anonymous API to let anyone get the Words of God on the internet, let it be for an Android app or for your next Web Project.

## Features

The API has multiple translations and commentaries in two languages: English and Hindi.
There is also available chapters meanings and summaries (Hindi only). 

## API Routes and Endpoints

By making a `GET` request to the API homepage (`/`) you get an answer with all the routes available. 

`$ curl https://bhagavadgita.theaum.org/`

```json
{
"/text/:ch/:verse": "Get text by chapter and verse",
"/text/translations/:ch/:verse": "Get text translations by chapter and verse",
"/text/transliterations/:ch/:verse": "Get text transliterations by chapter and verse",
"/text/commentaries/:ch/:verse": "Get text commentaries by chapter and verse",
"/chapter/:ch": "Get chapters",
"/chapter/transliteration/:ch": "Get chapters transliterations",
"/chapter/translation/:ch": "Get chapters translations",
"/chapter/meaning/:ch": "Get chapter meaning",
"/chapter/summaries/:ch": "Get chapter summaries"
}
```
## Examples 

Let's try to get the texts from Chapter 1, verse 1.

`$ curl https://bhagavadgita.theaum.org/text/1/1`

```json
{
  "data": [
    {
      "id": 1,
      "bg_id": "BG1.1",
      "chapter": "1",
      "verse": "1",
      "shloka": "धृतराष्ट्र उवाच |\nधर्मक्षेत्रे कुरुक्षेत्रे समवेता युयुत्सवः |\nमामकाः पाण्डवाश्चैव किमकुर्वत सञ्जय ||१-१||"
    }
  ]
}

```

Now, what does that mean? Let's try to hit the `translations` endpoint!

`$ curl https://bhagavadgita.theaum.org/text/translations/1/1`

```json
{
  "data": [
    {
      "id": 1,
      "bg_id": "BG1.1",
      "lang": "hi",
      "name": "Swami Tejomayananda",
      "author": "Swami Tejomayananda",
      "translation": "।।1.1।।धृतराष्ट्र ने कहा -- हे संजय ! धर्मभूमि कुरुक्षेत्र में एकत्र हुए युद्ध के इच्छुक (युयुत्सव:) मेरे और पाण्डु के पुत्रों ने क्या किया?"
    },
    {
      "id": 2,
      "bg_id": "BG1.1",
      "lang": "en",
      "name": "Swami Sivananda",
      "author": "Swami Sivananda",
      "translation": "1.1 Dhritarashtra said  What did my people and the sons of Pandu do when they had assembled\ntogether eager for battle on the holy plain of Kurukshetra, O Sanjaya."
    },
    {
      "id": 3,
      "bg_id": "BG1.1",
      "lang": "en",
      "name": "Shri Purohit Swami",
      "author": "Shri Purohit Swami",
      "translation": "1.1 The King Dhritarashtra asked: \"O Sanjaya! What happened on the sacred battlefield of Kurukshetra, when my people gathered against the Pandavas?\""
    },
    {
      "id": 4,
      "bg_id": "BG1.1",
      "lang": "en",
      "name": "Dr.S.Sankaranarayan",
      "author": "Dr.S.Sankaranarayan",
      "translation": "1.1. Dhrtarastra said  O Sanjaya ! What did my men and the sons of Pandu do in the Kuruksetra, the field of  righteousness, where the entire warring class has assembled ?\nor\nO Sanjaya !  What did the selfish intentions and the intentions born of wisdom do in the human body which is the field-of-duties,  the repository of the senseorgans and in which all the murderous ones (passions and asceticism etc.) are confronting [each other]."
    },
    {
      "id": 5,
      "bg_id": "BG1.1",
      "lang": "en",
      "name": "Swami Adidevananda",
      "author": "Swami Adidevananda",
      "translation": "1.1 Dhrtarastra said  On the holy field of Kuruksetra, gathered together eager for battle, what did my people and the Pandavas do, O Sanjaya?"
    },
    {
      "id": 6,
      "bg_id": "BG1.1",
      "lang": "en",
      "name": "Swami Gambirananda",
      "author": "Swami Gambirananda",
      "translation": "1.1. Dhrtarastra said  O Sanjaya, what did my sons (and others) and Pandu's sons (and others) actually do when, eager for battle, they assembled on the sacred field, the Kuruksetra (Field of the Kurus)?"
    },
    {
      "id": 7,
      "bg_id": "BG1.1",
      "lang": "hi",
      "name": "Swami Ramsukhdas",
      "author": "Swami Ramsukhdas",
      "translation": "।।1.1।। धृतराष्ट्र बोले (टिप्पणी प0 1.2) - हे संजय! (टिप्पणी प0 1.3) धर्मभूमि कुरुक्षेत्र में युद्ध की इच्छा से इकट्ठे हुए मेरेे और पाण्डु के पुत्रों ने भी क्या किया?"
    },
    {
      "id": 8,
      "bg_id": "BG1.1",
      "lang": "en",
      "name": "Sri Ramanuja",
      "author": "Sri Ramanuja",
      "translation": "1.1 - 1.19 Dhrtarastra said - Sanjaya said  Duryodhana, after viewing the forces of Pandavas protected by Bhima, and his own forces protected by Bhisma conveyed his views thus to Drona, his teacher, about the adeacy of Bhima's forces for conering the Kaurava forces and the inadeacy of his own forces for victory against the Pandava forces. He was grief-stricken within.\n\nObserving his (Duryodhana's) despondecny, Bhisma, in order to cheer him, roared like a lion, and then blowing his conch, made his side sound their conchs and kettle-drums, which made an uproar as a sign of victory. Then, having heard that great tumult, Arjuna and Sri Krsna the Lord of all lords, who was acting as the charioteer of Arjuna, sitting in their great chariot which was powerful enough to coner the three worlds; blew their divine conchs Srimad Pancajanya and Devadatta. Then, both Yudhisthira and Bhima blew their respective conchs separately. That tumult rent asunder the hearts of your sons, led by Duryodhana. The sons of Dhrtarastra then thought, 'Our cause is almost lost now itself.' So said Sanjaya to Dhrtarastra who was longing for their victory.\n\nSanjaya said to Dhrtarastra:  Then, seeing the Kauravas, who were ready for battle, Arjuna, who had Hanuman, noted for his exploit of burning Lanka, as the emblem on his flag on his chariot, directed his charioteer Sri Krsna, the Supreme Lord-who is overcome by parental love for those who take shelter in Him who is the treasure-house of knowledge, power, lordship, energy, potency and splendour, whose sportive delight brings about the origin, sustentation and dissolution of the entire cosmos at His will, who is the Lord of the senses, who controls in all ways the senses inner and outer of all, superior and inferior - by saying, 'Station my chariot in an appropriate place in order that I may see exactly my enemies who are eager for battle.'"
    },
    {
      "id": 9,
      "bg_id": "BG1.1",
      "lang": "en",
      "name": "Sri Abhinav Gupta",
      "author": "Sri Abhinav Gupta",
      "translation": "1.1  Dharmaksetre etc. Here some [authors] offer a different explanation as1 :-Kuruksetra : the man's body is the ksetra i.e., the facilitator, of the kurus, i.e., the sense-organs. 2 The same is the field of all wordly duties, since it is the cuse of their birth; which is also the field of the righteous act that has been described as :\n\n'This is the highest righteous act viz., to realise the Self by means of the Yogas';\n\n\nand which is the protector4 [of the embodied Self] by achieving emancipation [by means of this], through the destruction of all duties. It is the location where there is the confrontation among all ksatras, the murderous ones-because the root ksad means 'to kill' - viz, passion and asceticism, wrath and forbearance, and others that stand in the mutual relationship of the slayer and the slain. Those that exist in it are the mamakas,-i.e., the intentions that are worthy of man of ignorance and are the products of ignorance-and those that are born of Pandu: i.e., the intentions, of which the soul is the very knowledge itself5 and which are worthy of persons of pure knowledge. What did they do? In other words, which were vanished by what? Mamaka : a man of ignorance as he utters [always] 'mine'6. Pandu : the pure one.7"
    },
    {
      "id": 10,
      "bg_id": "BG1.1",
      "lang": "en",
      "name": "Sri Shankaracharya",
      "author": "Sri Shankaracharya",
      "translation": "1.1 Sri Sankaracharya did not comment on this sloka. The commentary starts from 2.10."
    },
    {
      "id": 11,
      "bg_id": "BG1.1",
      "lang": "hi",
      "name": "Sri Shankaracharya",
      "author": "Sri Shankaracharya",
      "translation": "।।1.1।।Sri Sankaracharya did not comment on this sloka."
    }
  ]
}

```
## Technical information 

The REST API has a very strong **caching policy** to allow latest latency possible all over the world. 

```
2022-01-21T16:00:15.772 app[348d4703] cdg [info] [GIN] 2022/01/21 - 16:00:15 | 200 | 150.994µs | {REMOTE_IP} | GET "/text/translations/1/1"
```
As you can see `150.994µs` is the time needed to query the cache database for the translation.

## Tech Stack

The API is written in **Golang** by using the [GIN framework](https://github.com/gin-gonic/gin) and [Gorm](https://gorm.io/index.html).
The Database is **SQLite**.
The project runs on **Cloudflare** and [Fly.io](https://fly.io/)

## Support 
[TheAum.org](https://theaum.org/) and [The Bhagavad Gita API](https://bhagavadgita.theaum.org/) doesn't earn a single penny from **Ads**, **you will never find them** on our pages and domains. 
However running these websites isn't **free**. 
Running servers **costs** in terms of **Bandwidth** and **CPU usage** to handle the traffic. 
If you can please donate to help the project keep going. 

If you wish to support us you can click the following button:

[![Buy Me A Coffee][2]][1]

[1]: https://www.buymeacoffee.com/theaum
[2]: https://cdn.buymeacoffee.com/buttons/default-black.png