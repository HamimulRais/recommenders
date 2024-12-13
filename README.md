# Machine Learning - Seefud

## Deskripsi Proyek
Each user access generates interaction data (searches, browsing, purchases, ratings) which is collected, cleaned, and processed to extract relevant features (product and user). This data is then used to train a recommendation model (e.g., content-based, collaborative, or hybrid) that predicts user preferences and generates relevant product recommendations, which are subsequently presented to the user. User feedback on these recommendations (clicks, purchases, ratings) is used to continuously improve the accuracy of the recommendation system.
This project aims to build a **recommendation system** using the following dataset:
1. **`product3.csv`**: This CSV file contains information about each individual product. The exact columns will vary depending on the dataset, but it will likely include at least a unique product identifier (e.g., a product ID) and potentially.
2. **`user3.csv`**: This CSV file records the interactions between users and products. The key aspect is the InteractionType column, where a value of 1 signifies an interaction.

## Build Model
- **String Encoding**: Before a machine learning model can process user and product IDs, which are typically strings, they need to be converted into numerical representations. StringLookup (likely from TensorFlow or a similar library) is a technique to create a mapping between the unique string IDs (user IDs and product IDs) and numerical indices. This creates a vocabulary where each unique ID gets assigned a unique integer. This numerical representation is crucial because machine learning models operate on numerical data. The StringLookup layer handles this efficiently, especially for large datasets with many unique IDs.
- **Model Buildingl**: A TensorFlow model is constructed to learn the relationships between users and products. This typically involves creating embedding layers for both users and products. An embedding layer transforms the numerical IDs (from the StringLookup) into dense, low-dimensional vector representations (embeddings). These embeddings capture latent features and relationships between users and products. The model then learns to predict the probability of an interaction between a user and a product based on their embeddings. Common architectures include matrix factorization, neural collaborative filtering, or more complex deep learning models. The model is trained using the interaction data (user3.csv), aiming to minimize the difference between predicted and actual interactions..
- **Model Conversion**: The trained TensorFlow model needs to be saved in a format suitable for deployment. TensorFlow SavedModel is a standard format that preserves the model's architecture and weights. This allows for easy loading and serving of the model in various environments. Alternatively, TensorFlow Lite (TFLite) can be used to convert the model into a more compact and optimized format for deployment on mobile devices or edge devices with limited resources..
- **Recommendation Generation**: Once the model is trained and saved, it can be used to generate recommendations. Given a user ID, the model retrieves the user's embedding and calculates the similarity or predicted interaction probability with all products in the catalog. The products with the highest predicted interaction probabilities are then presented as recommendations to the user. This process leverages the learned patterns in the user-product interaction data to suggest items that the user is likely to be interested in. The ranking of recommendations is crucial for presenting the most relevant items first..

## Instalation
Install all dependencies:
   ```bash
   pip install numpy pandas tensorflow
   ```

You can then access capstone3.ipynb to build the model to save and convert the model. 

