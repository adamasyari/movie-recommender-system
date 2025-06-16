# 🎬 Movie Recommender System with TensorFlow

Sistem rekomendasi film menggunakan pendekatan **Neural Collaborative Filtering (NCF)** dan dataset **MovieLens**. Proyek ini dibangun dengan **TensorFlow** untuk memprediksi rating pengguna terhadap film dan menghasilkan rekomendasi personalisasi.

---

## 📚 Dataset

Dataset yang digunakan adalah **MovieLens** dari GroupLens, tersedia di Kaggle:

- [MovieLens 100K Dataset](https://www.kaggle.com/datasets/grouplens/movielens-100k)
- [MovieLens 20M Dataset](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset)

File utama:
- `ratings.csv` — berisi userId, movieId, rating, timestamp

- `movies.csv` — berisi movieId, title, genres

---

## 🧠 Model

Model dibangun dengan arsitektur Neural Collaborative Filtering menggunakan `tf.keras`:

- **Input**: user ID dan movie ID
- **Embedding layer** untuk user dan movie
- **Concatenate layer** gabungan embedding
- **Dense layers** untuk belajar interaksi non-linear
- **Output**: prediksi rating antara 0.5–5.0

### Arsitektur

```text
User ID → Embedding →       →
                         ⟶ Concatenate → Dense → Dense → Output (Rating)
Movie ID → Embedding →       →
