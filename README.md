# wine-recommendation-system

## Business Impact

The current system effectively shows wines in a random or popularity‑only order. This leads to two issues for the company: many customers see wines that are not tailored to their tastes and a large portion of the catalog rarely appears on the first page. Our recommendation systems address both problems.

In our offline evaluation, the random baseline has essentially zero ranking quality: relevant wines almost never appear in the top‑10 positions. A popularity‑only recommender performs better but still misses many relevant items for many users. In contrast, our ALS‑based collaborative filter, content‑based models (BoW, TF‑IDF, lemmatization, NER, BERT), and especially the hybrid/context‑aware variants achieve much higher Accuracy@K and NDCG@K. In practical terms, this means users are far more likely to see relevant wines in their first page of recommendations than under random or popularity‑only display.

The popularity baseline tends to recommend the same small set of wines to almost everyone, resulting in very low catalog coverage. Our personalized models, and particularly the hybrid/context‑aware recommenders, surface thousands of distinct wines across users and reach substantially higher catalog coverage. This gives a much larger share of the catalog – including long‑tail and less well‑known wines – a chance to be seen and sold, rather than concentrating exposure on a handful of best‑sellers.

For users with enough historical ratings, the collaborative‑filtering and content‑based user‑to‑item models learn individual taste profiles and recommend wines that better match each user’s past choices. The hybrid TF‑IDF+ALS and context‑aware ALS variants in particular show high personalization scores in our evaluation, indicating that different users receive distinct recommendation lists rather than the same global top wines. This improves the perceived relevance of the recommendations for engaged users compared with a one‑size‑fits‑all list.

Overall, the system moves the company from a one‑size‑fits‑all display strategy to a data‑driven recommendation engine that increases the likelihood that users encounter relevant wines early in their journey, exposes a much larger portion of the catalog, supporting long‑tail and niche products, and adapts recommendations to individual tastes when sufficient historical data is available. These effects translate into more efficient use of the existing catalog and a better customer experience than the current randomized or purely popularity‑based approach, and they provide a solid foundation for future online experiments to quantify conversion and revenue uplift.

## Make sure to first run the notebooks in the preprocessing folder
