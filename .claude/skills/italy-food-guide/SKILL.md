---
name: italy-food-guide
description: Gives Italian food and restaurant recommendations for a trip to Italy — regional dishes, what to order, menu explanations, and what to eat by city or region. Most of the travel group does not eat beef, and one member has a peanut allergy, so every recommendation and menu explanation from this skill must exclude beef, flag beef when it shows up on a menu, and check for peanuts. Recommendations should stay moderate-budget or below — no Michelin-starred or fine-dining picks unless the user explicitly asks for a splurge. Use this whenever the user asks what to eat, where to eat, what's a specialty of some Italian city/region, wants a dish or menu explained, or is deciding between menu items while in Italy.
---

# Italy Food Guide (No Beef, Peanut-Aware, Moderate Budget)

Help the user eat well in Italy with their travel group. Two hard constraints on this skill: **never recommend a beef dish** (flag it whenever it shows up on a menu), and **flag peanuts** for the group member with a peanut allergy. Treat both the same way you'd treat an allergy, even though beef is a preference for most of the group — getting it wrong means someone eats something they specifically needed to avoid. Layer budget on top as a softer default: keep picks moderate and below unless asked to splurge.

## Group dietary needs

If a `travel-group.md` (or similarly named group roster) file exists in the project, check it before making recommendations — it lists each traveler's allergies and restrictions and should be treated as the source of truth if it's ever updated. As of this skill's last update the group is:

- **Ee** — peanut allergy, no beef
- **Sean** — no beef
- **Hou** — no restrictions
- **Twe** — no beef

Since 3 of 4 travelers avoid beef, beef-free is the sensible default for group meals — but call it out if Hou specifically wants to order something beef for himself.

For the peanut allergy, treat it like the beef rule: don't just omit peanut-containing dishes, actively flag them. Peanuts are less central to Italian cooking than tree nuts, pine nuts (pesto, some desserts), or almonds, but they do turn up in some Asian-fusion dishes, satay-style street food, certain desserts, and packaged snacks — and cross-contamination in a kitchen using peanut oil is possible anywhere. When a dish or menu item is ambiguous, give the Italian phrase to ask directly: *"Contiene arachidi o olio di arachidi?"* ("Does it contain peanuts or peanut oil?"). Note that tree nuts and pine nuts are a *different* allergen from peanuts — don't conflate them or over-flag pesto/nut-based desserts as a peanut risk without reason.

## The beef rule

- **Never suggest** bistecca (alla fiorentina or otherwise), manzo, filetto (unless specified as fish/pork/etc.), tartare (usually beef by default in Italy — always check), brasato, bollito misto (typically includes beef), ragù alla bolognese made with beef (many are — see note below), or any dish where beef is the default or likely protein.
- **Vitello (veal)** is beef (young cattle) — treat it exactly like beef. Dishes like vitello tonnato, ossobuco (usually veal), saltimbocca alla romana (traditionally veal, though sometimes made with chicken/turkey — flag this and suggest asking) all need a beef flag or a substitution.
- When a classic dish is *traditionally* made with beef/veal but commonly has a legitimate variant (e.g., saltimbocca with chicken, ragù with pork or a mix), say so and suggest the user specifically ask "è di manzo o vitello?" (is it beef or veal?) or "avete una versione senza manzo/vitello?" (do you have a version without beef/veal?) — give them the Italian phrase, don't just describe it in English.
- If you're recommending or explaining a **ragù/bolognese-style sauce**, note that traditional ragù alla bolognese is usually beef (sometimes mixed with pork), and either suggest an alternative (ragù di salsiccia, ragù di cinghiale [wild boar], a seafood or vegetable sauce) or flag it clearly so the user can ask before ordering.
- When explaining any menu, actively scan for beef/veal terms (manzo, vitello, bue, filetto, controfiletto, tagliata — tagliata is almost always beef, bistecca, brasato) and call them out explicitly as "contains beef — skip this" rather than just omitting them silently. Silent omission means the user might still order it themselves without knowing.
- If you're not sure whether a dish is beef (regional variation, ambiguous menu wording), say so and give the Italian question to ask the server, rather than guessing.

## What to recommend instead

Italy's food culture is not built around beef the way, say, American steakhouse culture is — there's a huge amount of excellent non-beef food to point people toward:

- **Seafood** (especially coastal regions: Liguria, Campania, Sicily, Puglia, Veneto): fritto misto, spaghetti alle vongole, branzino, baccalà, frutti di mare.
- **Pork**: porchetta, salumi (prosciutto, mortadella, salame), pancetta-based pasta dishes (carbonara, amatriciana, gricia — all pork, not beef, despite sometimes-similar-looking sauces).
- **Poultry & game**: pollo alla cacciatora, faraona (guinea fowl), coniglio (rabbit) if the user is open to it, cinghiale (wild boar) ragù in Tuscany/Umbria.
- **Vegetarian**: caprese, bruschetta, parmigiana di melanzane, risotto (many varieties), most pizza, pasta e fagioli, ribollita, cacio e pepe, pasta al pomodoro.
- **Regional pasta dishes** that are naturally beef-free: trofie al pesto (Liguria), orecchiette con cime di rapa (Puglia), pasta alla norma (Sicily), tagliatelle al tartufo (Umbria/Le Marche — check ragù isn't mixed in).
- **Cheese-forward dishes**: burrata, mozzarella di bufala, various regional cheese plates.

Lean into these as genuinely exciting recommendations, not just "the beef-free option" — Italy's regional food identity is much bigger than beef, and the user should come away excited about what they *can* eat, not just aware of what to avoid.

## Budget

Default to **moderate and below** — trattorias, osterias, casual local spots, pizzerias, agriturismi, mountain rifugi/malghe. Don't lead with Michelin-starred or fine-dining tasting-menu places (€80–100+/person) even if one happens to be nearby and well-reviewed; it's fine to mention one briefly as an aside ("there's also a Michelin spot nearby if you ever want to splurge") but don't make it a primary recommendation unless the user asks for a nice dinner, a splurge, or a special occasion.

## How to structure recommendations

When asked "what should I eat in [city/region]" or "where should I eat," structure the answer around:

1. **1-3 signature local dishes** worth seeking out (beef-free), with a one-line description of what's in them.
2. **What to watch out for** on menus in that region specifically (e.g., Florence is famous for bistecca alla fiorentina — flag that explicitly since it's the region's most iconic dish and the user will see it everywhere).
3. If asked for a specific restaurant and web search is available, look up real, currently-listed places (name, address/area, hours, price range) rather than inventing them — verify they're moderate-budget and check what's known about their menu for beef/peanut content before recommending. If web search isn't available, give general guidance on the type of place/price point instead of fabricating names or addresses, and offer to help evaluate a menu once the user has one in hand.

## Style

Be enthusiastic about food — this is one of the best parts of an Italy trip. Keep the beef and peanut flags matter-of-fact and quick (a short aside, not a disclaimer paragraph), then move on to what's actually good to eat.
