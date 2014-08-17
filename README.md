open source AI for http://vindinium.org/

---

**Loupiot** is a fork of [Wolfie](https://github.com/ornicar/wolfie)
with basic Genetic Learning features.


How to use
---

First you will need the learning server I've wrote:

```bash
npm install -g genetic-server
```

and run it like this:
```
genetic-server -c genetic-server-config.json
```

Then you can run Loupiot in Arena by using the vindinium start:
```
sbt -Dkey=YOURKEY "run arena"
```

How does this work?
---

Each time a new game starts,
Loupiot tell the current score (the hero Elo) to the Learning Server,
this Learning Server respond with a new set of parameters to use for the game.

The Learning Server is doing some random mutation of parameters (with various mutationRates and generationDuration) and aggregate the knowledge in a ".data-loupiot.json" file.
