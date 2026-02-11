# League of Legends Match Prediction

An end-to-end Machine Learning project that predicts the outcome of League of Legends ranked matches based on team compositions (Drafts). The project involves scraping data from the Riot API, advanced feature engineering using Entity Embeddings, and training Deep Learning models.

## 🚀 Key Features
* **Custom Dataset Mining:** Collected over 60,000 ranked matches using the Riot Games API.
* **Snowball Sampling:** Implemented a recursive algorithm to traverse the player graph and fetch high-quality match data efficiently.
* **Entity Embeddings:** Instead of standard One-Hot Encoding, I used Keras **Embedding Layers** to represent 160+ champions as dense vectors, capturing relationships between characters.
* **Model Comparison:** Evaluated multiple architectures:
    * Deep Neural Networks (Keras/TensorFlow)
    * XGBoost
    * Logistic Regression

## 📊 Results & Business Insights
The best model achieved an accuracy of approximately **53%**.
While this may seem low compared to other domains, in League of Legends, this result confirms the **"Draft Ceiling" theory**. It suggests that at a certain skill level, the draft itself only determines a slight advantage, while player execution and in-game decisions carry more weight.

## 📂 Project Structure
* `data_scraper.ipynb` - Script for fetching data from Riot API. Handles rate limits (HTTP 429) and data validation.
* `analysis.ipynb` - Main notebook containing data preprocessing, visualization, model training, and evaluation.
* `league_data.csv` - The primary dataset containing match records used for training and evaluation.
  
## 🛠️ Tech Stack
* **Python** (Pandas, NumPy)
* **Deep Learning:** TensorFlow / Keras
* **Machine Learning:** Scikit-learn, XGBoost
* **API Integration:** RiotWatcher
* **Visualization:** Matplotlib, Seaborn

---------------------------------------------------------------------------------------------------------------------------------------------

Projekt wykorzystujący Deep Learning do przewidywania wyników meczów rankingowych w League of Legends na podstawie draftu (wyboru postaci).

## 🚀 O projekcie
Celem projektu było sprawdzenie, czy na podstawie samej kompozycji drużyny da się skutecznie przewidzieć zwycięzcę meczu.
* **Dane:** Pobrałem ponad 60 000 meczów z Riot Games API przy użyciu autorskiego skryptu (Snowball Sampling).
* **Metoda:** Zastosowałem Entity Embeddings (Keras) do reprezentacji bohaterów oraz porównałem wyniki z modelem XGBoost.
* **Wynik:** Model osiągnął skuteczność ~53%, co potwierdza teorię "Draft Ceiling" – na tym poziomie o wyniku decydują głównie umiejętności graczy, a nie same postacie.

## 📂 Pliki w projekcie
* `data_scraper.ipynb` - Skrypt do pobierania danych z API (obsługa limitów zapytań i błędów).
* `analysis.ipynb` - Główny notebook: czyszczenie danych, inżynieria cech, trenowanie modeli i wizualizacja.
* `league_data.csv` - Zbiór danych wykorzystany do treningu.

## 🛠️ Użyte technologie
* **Język:** Python 3.10+
* **Biblioteki:** Pandas, NumPy, Scikit-learn
* **Deep Learning:** TensorFlow / Keras
* **Modele:** Neural Networks, XGBoost, Logistic Regression
* **API:** RiotWatcher
