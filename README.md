# “Mirror, Mirror on My Feed, What Emotions Do We Reinforce and Need”: Emotional Mirroring in Eating Disorder Content on TikTok

This repository contains supporting resources for our the paper “Mirror, Mirror on My Feed, What Emotions Do We Reinforce and Need”: Emotional Mirroring in Eating Disorder Content on TikTok 

It includes:

1. **Non-Eating Disorder (Non-ED) Video Dataset (non_ed_data.csv)**
2. **Code for Constructing the User Similarity Network (user_similarity_network.py)**

---

## 1. Non-ED TikTok Video Dataset

This dataset includes TikTok video IDs that are unrelated to eating disorders. Videos were selected by filtering out any mention of ED-related terms.

---

## 2. User Similarity Network Construction

To understand community dynamics and emotional mirroring in user interactions, we built a user similarity network based on commenting behavior.

### Overview of Method
We implemented the methodology adapted from Luceri et al. (2024) to construct the network:

- **Step 1:** Build a **bipartite graph** where:
  - One node set = TikTok users
  - Second node set = TikTok videos
  - Edges = when a user comments on a video
- **Step 2:** Compute **TF-IDF** scores for each user-video edge to reflect video popularity.
- **Step 3:** Project the bipartite graph into a **user-user similarity graph** using **cosine similarity**.
- **Step 4:** Remove self-loops and isolated nodes to ensure meaningful interactions.

- Requires `networkx`, `scikit-learn`, and `community` (python-louvain) packages.

### Output
- A weighted graph representing user similarity based on shared commenting patterns.

---

## Citation

If you use this dataset or code, please cite:

> Anonymous. “Mirror, Mirror on My Feed, What Emotions Do We Reinforce and Need”: Emotional Mirroring in Eating Disorder Content on TikTok
---

## License

This repository is intended for academic use only and complies with TikTok's Research API Terms of Service. No identifiable user information is included.

