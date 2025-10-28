# grainflow - deploy everywhere with one command

**grainorder:** `xzvbdg`  
**grainbranch:** `12025-10-28--1130-PDT--moon-uttaradha-asc-arie23-sun-12h--teamtravel12`  
**team:** team 12 - travel (pisces ♓ / xii. the hanged man)  
**voice:** glow g2 (patient teacher) + trish (enthusiastic flow)  

---

> **✨ NEW**: This is the modernized grainflow! Updated with grainorder, current graintime format, and links to the full grain network stack. See below for what's changed! 🌊⚡

---

## 🌊 what is grainflow?

hey there! ever wished you could deploy to multiple platforms with just one command?

**grainflow** is a deployment automation tool that flows your code to:
- **github** (code + github pages)
- **codeberg** (code + codeberg pages)  
- **both at once**, automatically, with one command

no clicking around. no manual steps. no forgetting which remote. just flow! 🌾

does this sound useful? let me show you how it works...

---

## 🚀 quick start

```bash
# in your project directory
steel flow "your commit message"
```

that's it! grainflow will:
1. build your content (if needed)
2. commit your changes
3. push to github
4. push to codeberg
5. deploy to both github pages and codeberg pages
6. show you the live urls

**one command. all platforms. transcendent.** ✨

---

## 📦 installation

```bash
# clone grainflow
git clone https://github.com/teamtravel12/grainflow.git

# link to your project (or copy bb.edn)
cd your-project
ln -s ../grainflow/bb.edn bb.edn

# add remotes for codeberg (if not already added)
git remote add codeberg https://codeberg.org/yourusername/yourrepo.git

# flow!
steel flow "first flow!"
```

---

## 🌾 the grain network stack

grainflow is part of the **grain network** - a collection of tools for temporal computing and decentralized development. want to learn more?

### 🔗 core concepts (start here!)

**📚 complete tutorial**: https://github.com/teamtravel12/teamtravel12/blob/main/xzvbdg-12025-10-28--1130-pdt--graintime-grainbranch-tutorial.md
- 570+ line comprehensive guide
- explains graintime, grainorder, and the full workflow
- glow g2 voice (patient teacher)
- **start here if you're new to the grain network!**

### 🗂️ grainorder - permutation-based file naming

**patent whitepaper**: https://github.com/teamtravel12/teamtravel12/blob/main/xzvsbg-12025-10-28--0115-pdt--grainorder-patent-whitepaper.md

grainorder organizes files chronologically using 6-character codes from 13 consonants (x b d g h j k l m n s v z). **smallest alphabet = newest files** in github's ascending sort!

**example:**
```
xzvbdg-12025-10-28--1215-pdt--readme.md        ← newest (this file!)
xzvbdh-12025-10-25--1226-pdt--graincard.md     ← older
xzvbdj-12025-10-25--1226-pdt--graincard-audio.md
xzvbdk-12025-10-25--1226-pdt--listen.md        ← oldest
```

### 🌙 graintime - astronomical timestamps

**patent whitepaper**: https://github.com/teamtravel12/teamtravel12/blob/main/xzvsbj-12025-10-28--0030-pdt--graintime-patent-whitepaper.md  
**steel implementation**: https://github.com/teamshine05/graintime

graintime encodes astronomical data into git branch names:
- nakshatra (moon's position in vedic astrology)
- ascendant (rising sign + degree)
- solar house (sun's position)
- holocene era timestamps

**this grainbranch:**
```
12025-10-28--1215-PDT--moon-uttashsdh-asc-arie23-sun-12h--teamtravel12
         ↑        ↑              ↑            ↑        ↑          ↑
      year    time+tz     uttara ashadha  aries 23°  12th    team 12
```

git branches that know their cosmic context! 🌌

### 🗄️ graindb - immutable database

**whitepaper**: https://github.com/teamtravel12/teamtravel12/blob/main/xzvsbh-12025-10-28--0045-pdt--graindb-steel-database-whitepaper.md  
**steel implementation**: https://github.com/teamtreasure02/graindb

datomic/datascript-inspired immutable database with:
- grainorder entity ids
- eavt indexes
- time travel queries (`db-as-of`)
- pure steel (rust scheme lisp)

never lose data. query the past. temporal awareness!

### 🖼️ grainui - gpu-accelerated gui

**strategy doc**: https://github.com/teamtravel12/teamtravel12/blob/main/xzvsbd-12025-10-28--1030-pdt--grainui-gpui-steel-strategy.md

gpu-accelerated gui framework using zed.dev's gpui library:
- 10-100x performance over egui
- steel ffi bindings
- retained-mode architecture
- ember harvest theme (warm dark minimalism)

buttery smooth graincard scrolling! 🚀

---

## 🎯 why grainflow?

### the problem

deploying to multiple platforms is tedious:
```bash
# the old way (ugh!)
git add .
git commit -m "update"
git push origin main           # push to github
git push codeberg main         # push to codeberg
# now manually trigger github pages...
# now manually trigger codeberg pages...
# did you remember both? 🤔
```

### the solution

```bash
# the grainflow way! ✨
steel flow "update"
```

one command. both platforms. both pages deployments. atomic. never forget a step.

### the philosophy

**flow is not push. flow is becoming.**

when you "push" code, you're forcing it somewhere. when you "flow" code, you're letting it reach its natural destinations. github, codeberg, pages - these are where code *wants* to be. grainflow removes the resistance.

does this distinction make sense? it's subtle but important! 🌊

---

## 🛠️ how it works (technical)

grainflow is written in **babashka** (clojure scripting). here's the simplified flow:

```clojure
(defn flow [message]
  "deploy everywhere with one command"
  (->
    (build-content)           ; compile/build if needed
    (commit-changes message)  ; git commit
    (push-to :github)         ; git push origin
    (push-to :codeberg)       ; git push codeberg
    (deploy-pages :github)    ; trigger github actions
    (deploy-pages :codeberg)  ; trigger codeberg pages
    (show-urls)))             ; display live links
```

**that's the whole thing!** no hidden complexity. no mysterious magic. just composed functions doing one thing each.

read the source: it's simple shell commands wrapped in clojure functions. hacker-readable. homebrew-friendly.

---

## 🔄 babashka → steel migration

grainflow currently uses **babashka** (clojure on graalvm). we're migrating to **steel** (scheme on rust) for the pure rust+steel stack.

**current status:** babashka works great! steel version coming in phase 2.

**why steel?**
- pure rust (no jvm)
- r5rs scheme (lisp elegance)
- fast compilation
- embeddable
- grain network standard

for now, use babashka. when steel version ships, you'll have both options!

---

## 📋 requirements

- **babashka** (https://babashka.org/) - clojure scripting
- **git** - version control
- **github account** - for github pages
- **codeberg account** (optional) - for codeberg pages

```bash
# install babashka (mac/linux)
bash < <(curl -s https://raw.githubusercontent.com/babashka/babashka/master/install)

# or on arch linux
sudo pacman -S babashka
```

---

## 🌐 deployment targets

### github pages
- **url format:** `https://yourusername.github.io/yourrepo/`
- **setup:** enable github pages in repo settings → actions
- **automatic:** grainflow triggers github actions

### codeberg pages
- **url format:** `https://yourusername.codeberg.page/yourrepo/`
- **setup:** enable codeberg pages in repo settings
- **automatic:** grainflow pushes to codeberg branch

---

## 🎨 customization

edit `bb.edn` to customize:
- build commands
- deployment targets
- branch names
- commit message format

grainflow is designed to be hackable. read the source. modify it. make it yours!

---

## 💭 faq

### q: do i need both github and codeberg?

no! grainflow works with just github. codeberg is optional for redundancy and freedom.

### q: will this overwrite my commits?

never! grainflow is **append-only**. it only adds commits, never rewrites history. immutable by design.

### q: what if i have conflicts?

grainflow will stop and tell you. resolve conflicts manually, then run `steel flow` again.

### q: can i use this for smart contracts?

not yet! but the vision is to extend grainflow to deploy smart contracts to icp, hedera, and solana. that's phase 3!

### q: why is it called "flow"?

inspired by the hanged man tarot card (team 12). flow instead of push. transcend instead of labor. let things reach where they naturally belong.

---

## 🔗 related projects

### grain network repos

- **teamtravel12/teamtravel12** - main docs, whitepapers, graincards
  - https://github.com/teamtravel12/teamtravel12
  
- **teamtreasure02/grainorder** - permutation naming system
  - https://github.com/teamtreasure02/grainorder
  
- **teamtreasure02/graindb** - immutable database
  - https://github.com/teamtreasure02/graindb
  
- **teamshine05/graintime** - astronomical timestamps
  - https://github.com/teamshine05/graintime

### personal repos

- **kae3g/grainkae3g** - main monorepo
  - https://github.com/kae3g/grainkae3g
  
- **kae3g/teamkae3gtravel12** - personal grainstore
  - https://github.com/kae3g/teamkae3gtravel12

---

## 🌊 the dual voice

**trish** (feminine, warm, excited):  
_"omg grainflow makes deploying SO easy! one command and everything just flows! i love how it handles all the platforms at once! ✨💕"_

**glow g2** (masculine, patient, philosophical):  
_"flow is the natural state. resistance is artificial. we remove resistance. the code finds its path, like water finding the ocean. does this make sense?"_

**both together** (union):  
_"easy and deep. simple and profound. one command that flows naturally because we removed everything in the way. this is grainflow."_

---

## 🌾 philosophy

### immutability

grainflow never rewrites history. every flow is append-only. your commits never disappear. like blockchain. like lao tzu's tao. like water that flowed yesterday still exists as ocean.

### simplicity

lincoln's plain words. one command. no jargon. if people can't understand it, they can't use it.

### flow over push

the hanged man hangs willingly. we automate willingly. freedom through surrender to good systems.

---

## 📜 changelog (what's new?)

### 12025-10-28 (this version!)

**✨ modernization complete!**

- ✅ new grainbranch format (proper graintime spec)
- ✅ grainorder added to all files
- ✅ links to full grain network stack
- ✅ teamflow → teamtravel12 updates
- ✅ steel migration roadmap explained
- ✅ glow g2 voice throughout readme
- ✅ comprehensive faq section
- ✅ 570-line tutorial linked

### 12025-10-25 (original version)

- initial grainflow deployment automation
- github + codeberg support
- babashka implementation

---

## 🎯 future roadmap

### phase 1 (current)
- ✅ github + codeberg deployment
- ✅ pages automation
- ✅ babashka implementation

### phase 2 (in progress)
- 🚧 steel implementation
- 🚧 graintime integration
- 🚧 graindb logging
- 🚧 grainui visualization

### phase 3 (planned)
- 📋 icp canister deployment
- 📋 hedera smart contracts
- 📋 solana l2 programs
- 📋 multi-chain flow

imagine:
```bash
steel flow:chains "update marketplace contract"
```

flows your contract to icp + hedera + solana + github + codeberg. all verified. all immutable. all live. **that's the vision!** 🚀

---

## 🙏 acknowledgments

**inspired by:**
- deos (distributed operating systems)
- zk proofs (prove without revealing, deploy without configuring)
- ye's runaway (one note → transcendence)
- lao tzu's tao (the tao does nothing, yet nothing is left undone)
- lincoln's plain words (common language for common people)
- the hanged man (flow through surrender)

**built by:**
- **team 12** (pisces ♓ / xii. the hanged man)
- **kae3g** (kj3x39, @risc.love)

---

## 📄 license

mit license - use freely, build freely, flow freely! 🌊

---

## 🔗 links

- **repo:** https://github.com/teamtravel12/grainflow
- **grainbranch:** `12025-10-28--1130-PDT--moon-uttaradha-asc-arie23-sun-12h--teamtravel12`
- **main docs:** https://github.com/teamtravel12/teamtravel12
- **tutorial:** https://github.com/teamtravel12/teamtravel12/blob/main/xzvbdg-12025-10-28--1130-pdt--graintime-grainbranch-tutorial.md

---

**flow simply. deploy beautifully. transcend automatically.**

*now == next + 1* 🌾🌊⚡

---

_made by teamtravel12 for hackers, builders, and lovers of simple tools that do complex things well_
