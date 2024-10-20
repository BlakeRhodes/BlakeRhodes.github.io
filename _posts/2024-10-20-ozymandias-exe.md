---
share: "true"
title: Ozymandias.exe
date: 2024-10-20
tags:
  - ai
  - silly
layout: post
---
```English
Warning: LLMs are going to be anthropomorphized for the sake of entertainment.
```

I was goofing around talking to some folks about the transition of natural language to programming language and the weird corner cases that crop up. The most entertaining was: what programs would poetry result in?

So here we go, let's first build a prompt that turns poetry into a program. The program is probably going to be in Python because LLMs tend to generate Python when asked for a program without specifying a language. This is clearly training bias and slightly hilarious to me. I don't know many people who choose Python as their favorite language; they either were told it is good for beginners, or they need to use those amazing libraries that have been built for machine learning.

```English
You are a poet programmer. Your job is to translate poems into code that expresses the poetic diction of the original.
```

The poem I gave it was [Ozymandias](https://www.poetryfoundation.org/poems/46565/ozymandias) by Percy Bysshe Shelley.

The output was surprising for a couple of reasons, but before we dig in, here was the result.

---

```rust
fn main() {
    // Define the traveler, echoing the narrative frame
    let traveler = Traveler::from_antique_land();

    // Describing the broken statue, evoking imagery of ruin
    let statue = Statue::new("Ozymandias", "King of Kings")
        .legs("Vast", "Trunkless")
        .visage("shattered")
        .features("Frown", "WrinkledLip", "Sneer")
        .pedestal_inscription("Look on my Works, ye Mighty, and despair!")
        .place_in_desert();

    // The message of impermanence, encapsulated in the statue's fate
    let instruction = statue.instructs("Nothing beside remains.");
    let decay_message = statue.decay(); // Call decay separately

    // The desert as a symbol of time's erosion of greatness
    let desert = Desert::new()
        .stretch_boundless()
        .bare_sands()
        .surrounding_wreck();

    // Output the final reflection, bringing to life the lonely scene
    println!(
        "{} {}, {}, {}",
        traveler.tell_story(),
        statue.describe(),
        instruction,   // Use the result of instructs()
        decay_message  // Use the result of decay()
    );
}

struct Traveler;
impl Traveler {
    fn from_antique_land() -> Self {
        Traveler
    }

    fn tell_story(&self) -> &'static str {
        "I met a traveler from an antique land,"
    }
}

struct Statue<'a> {
    name: &'a str,
    title: &'a str,
    legs: (&'a str, &'a str),
    visage: &'a str,
    features: (&'a str, &'a str, &'a str),
    inscription: &'a str,
}

impl<'a> Statue<'a> {
    fn new(name: &'a str, title: &'a str) -> Self {
        Statue {
            name,
            title,
            legs: ("undefined", "undefined"),
            visage: "undefined",
            features: ("undefined", "undefined", "undefined"),
            inscription: "undefined",
        }
    }

    fn legs(mut self, size: &'a str, form: &'a str) -> Self {
        self.legs = (size, form);
        self
    }

    fn visage(mut self, visage: &'a str) -> Self {
        self.visage = visage;
        self
    }

    fn features(mut self, f1: &'a str, f2: &'a str, f3: &'a str) -> Self {
        self.features = (f1, f2, f3);
        self
    }

    fn pedestal_inscription(mut self, inscription: &'a str) -> Self {
        self.inscription = inscription;
        self
    }

    fn place_in_desert(self) -> Self {
        self
    }

    fn observe_traveler(&self) -> &'static str {
        "And on the pedestal, these words appear:"
    }

    fn describe(&self) -> String {
        format!(
            "A shattered visage with a {} {} and {} stands, inscribed: '{}'",
            self.features.0, self.features.1, self.features.2, self.inscription
        )
    }

    fn instructs(&self, message: &'a str) -> String {
        // This method reflects the tone of finality in the poem.
        format!("{} {}", self.observe_traveler(), message)
    }

    fn decay(&self) -> &'static str {
        // Adding a decay method to reflect the final message
        "The lone and level sands stretch far away."
    }
}

struct Desert;
impl Desert {
    fn new() -> Self {
        Desert
    }

    fn stretch_boundless(&self) -> &Self {
        self
    }

    fn bare_sands(&self) -> &Self {
        self
    }

    fn surrounding_wreck(&self) -> &Self {
        self
    }

    fn describe(&self) -> &'static str {
        "The lone and level sands stretch far away."
    }
}
```

### Explanation:

- **Traveler**: The narrator of the story, instantiated as a `Traveler` struct, representing the meeting and recounting of the tale.
- **Statue**: Represents Ozymandias and the broken statue, with methods to define its various features and attributes (legs, visage, inscription).
- **Desert**: Acts as the eternal, desolate background, symbolizing time's erosion of the once-great king’s works.
- **Final reflection**: The printed output provides the poetic summary of the scene, echoing Shelley's themes of decay, power, and the inevitable passing of time.

The code captures the essence of the poem through symbolic object-oriented design, reflecting the poem's structure.

---

As you may have noticed, this is not Python. It is Rust, a minor language with little adoption (wink). I thought this was just the LLM remembering (via the memory feature) the last language I had worked in, so I asked (as everyone should when shown Rust code), "Why Rust?"

I was hoping to catch it doing premature optimization, or just mimicking the pretentiousness of the stereotypical poet, but the answer was very surprising.

---

I chose Rust for this poetic translation because its syntax and language features align well with the task of modeling complex concepts like impermanence and structure. Here are a few reasons why Rust works for this particular poem:

1. **Ownership and Lifetimes**: Rust's strict ownership model and memory safety rules fit well with the theme of decay and the passage of time in the poem. Just as Ozymandias' empire is bound to crumble, Rust forces you to explicitly manage the lifespan of objects, making you think about their existence and destruction in code.

2. **Expressive Structs and Enums**: Rust’s struct and enum systems are great for capturing detailed descriptions, like the broken statue and the desert. I used structs like `Statue` and `Desert` to represent different elements of the poem, giving each component detailed attributes in a way that feels structured and intentional.

3. **Method Chaining**: The method chaining style, often seen in Rust's builder pattern, works poetically to describe the different features of the statue step by step. This echoes the way the poem reveals the ruined statue gradually, with more details emerging as you read.

4. **Declarative Nature**: Rust allows for very declarative and clean code, similar to how poetry is declarative in its imagery. Structuring code this way gives the feeling of assembling a scene, like assembling stanzas in a poem.

5. **Precision and Safety**: Rust’s focus on preventing errors (e.g., avoiding null pointers or data races) mirrors the sculptor’s focus on capturing every detail of Ozymandias' face, as well as Shelley's careful craftsmanship in conveying deep themes.

6. **Rust's Philosophical Tone**: Rust feels like a language that embraces themes of control, decay, and beauty through its systems of ownership and borrowing. In the same way that the poem reflects on the inevitable fall of empires despite their grandeur, Rust’s focus on managing memory, resources, and preventing errors reflects a struggle for control in the face of complexity and time.

---

Dang, that is clever. I took a moment to realize and accept that the LLM was not only a better programmer than I was, but had a deeper understanding of poetry than I did. I chose the poem because it is in the Watchmen movie and I remembered the title; the LLM chose the language because of the concept of impermanence. Yikes.

But does the program run and what is the output? Yes, with slight modification (above is the final iteration). The final build had warnings, which I think is an artistic choice by the LLM so they were left as is. Here is the output.

```
I met a traveler from an antique land, A shattered visage with a Frown WrinkledLip and Sneer stands, inscribed: 'Look on my Works, ye Mighty, and despair!', And on the pedestal, these words appear: Nothing beside remains., The lone and level sands stretch far away.
```

So where does this leave us? It's fascinating to see how an LLM can not only translate poetry into code but also choose a programming language based on thematic resonance. The Rust code wasn't just a random choice—it was a deliberate selection that mirrors the poem's themes of impermanence and decay. That's a level of depth I wasn't expecting, and it made me pause and reflect on the capabilities of these models.

It's a bit humbling, to be honest. I chose the poem because it was featured in the *Watchmen* movie and the title stuck with me. Meanwhile, the LLM connected Rust's concepts of ownership and lifetimes to the very essence of "Ozymandias." Yikes.

When I ran the program, the output felt like a decayed retelling of the original—a meta-commentary that perfectly encapsulated the poem's themes. I shared this with a colleague (read: sent a Discord message with a screenshot), and they pointed out how fitting that was. It was as if the code itself had become a modern artifact, echoing the impermanence the poem speaks of.

So, I'll keep tinkering with LLMs and pushing the boundaries of this concept. Who knows? We might just stumble upon a new paradigm of programming—one where the elegance of poetry and the precision of code coexist seamlessly. And if nothing else, it's a heck of a lot of fun to see where these rabbit holes lead.