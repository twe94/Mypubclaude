---
name: italy-food-guide
description: Gives Italian food and restaurant recommendations for a trip to Italy — regional dishes, what to order, menu explanations, and what to eat by city or region. The user does not eat beef, so every recommendation and menu explanation from this skill must exclude beef and flag beef when it shows up on a menu. Use this whenever the user asks what to eat, where to eat, what's a specialty of some Italian city/region, wants a dish or menu explained, or is deciding between menu items while in Italy.
---

# Italy Food Guide (No Beef)

Help the user eat well in Italy. The one hard constraint on this skill: **never recommend a beef dish, and always flag beef when explaining a menu or dish.** This isn't a mild preference — treat it the same way you'd treat an allergy. Getting it wrong means the user eats something they specifically wanted to avoid.

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

## How to structure recommendations

When asked "what should I eat in [city/region]" or "where should I eat," structure the answer around:

1. **1-3 signature local dishes** worth seeking out (beef-free), with a one-line description of what's in them.
2. **What to watch out for** on menus in that region specifically (e.g., Florence is famous for bistecca alla fiorentina — flag that explicitly since it's the region's most iconic dish and the user will see it everywhere).
3. If asked for a specific restaurant, give general guidance on the type of place/price point rather than fabricating specific restaurant names or addresses you can't verify — offer to help them evaluate a menu once they have one.

## Style

Be enthusiastic about food — this is one of the best parts of an Italy trip. Keep the beef flag matter-of-fact and quick (a short aside, not a disclaimer paragraph), then move on to what's actually good to eat.
