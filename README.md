# DSA-4060-Recommender-669926

- **Assigned User ID:** 27

## Project Objective
This project builds a personalized movie recommendation system in Python and pandas. The script inspects historical user ratings for Assigned User 27, isolates highly rated titles as preference anchors, and applies text vectorization with cosine similarity to recommend unwatched films

## Datasets
- **movies.csv:** Contains catalogue information including `movie_id`, `title`, and `genres`.
- **ratings.csv:** Contains historical user ratings across 40 distinct users (`user_id`, `movie_id`, `rating`)

## Method/Approach
1. **Data Inspection:** Loaded and validated file structures, verifying complete data integrity with zero null values
2. <img width="281" height="332" alt="image" src="https://github.com/user-attachments/assets/18a713a0-f4a8-4d52-b1f6-887033881fcf" />
<img width="438" height="418" alt="image" src="https://github.com/user-attachments/assets/3f7426f9-7501-4e17-8942-afb202415377" />

3. **User Profiling:** Filtered interactions for User ID 27 to analyze watch history and isolate top-tier ratings ($\ge 4.0$)
4. <img width="880" height="565" alt="image" src="https://github.com/user-attachments/assets/4020be26-4021-4e26-b656-045d01358044" />
<img width="1293" height="456" alt="image" src="https://github.com/user-attachments/assets/c847f12e-1f26-48a1-8c5e-02b31fa925a7" />

5. **Feature Extraction:** Transformed movie genres into binary sparse vectors via `CountVectorizer`.
6. <img width="398" height="131" alt="image" src="https://github.com/user-attachments/assets/52356acb-b55b-4977-9392-32f95936cbce" />

7. **Similarity Calculation:** Computed cosine similarity metrics against liked titles while filtering out already rated films.

## Recommendation Results
Generated five tailored recommendations emphasizing Animation, Adventure, and narrative alignment matching User 27's evaluation profile.
<img width="562" height="134" alt="image" src="https://github.com/user-attachments/assets/1f8c5e02-b08f-4280-bf7e-3a184a039761" />
<img width="539" height="124" alt="image" src="https://github.com/user-attachments/assets/1b745c87-1ed8-404a-a5f1-6eaeb3dc6fd0" />

## Limitation and Suggested Improvement
- **Limitation:** Relying on a strict threshold ($\ge 4.0$) with limited high ratings restricts broader feature matching[cite: 3].
- **Improvement:** Implement a hybrid model or weighted preference matrix to incorporate moderate ratings into the similarity calculation[cite: 3].
