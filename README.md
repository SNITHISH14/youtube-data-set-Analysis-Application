# youtube-data-set-Analysis-Application
import pandas as pd

def load_data(filepath):
    """
    Load dataset from the given CSV file path.
    """
    return pd.read_csv(filepath)

def preprocess_data(df):
    """
    Preprocess the dataset:
    - Drop irrelevant/non-numeric columns
    - Convert categorical variables using one-hot encoding
    - Handle missing values
    """
    df = df.copy()

    # Drop non-numeric or irrelevant columns
    columns_to_drop = [
        'Channel Name', 
        'Youtuber Name', 
        'Best Video', 
        'Neural Interface Compatible', 
        'Holographic Content Rating'
    ]
    df = df.drop(columns=columns_to_drop, errors='ignore')

    # Convert categorical column to dummy variables
    df = pd.get_dummies(df, columns=['Metaverse Integration Level'], drop_first=True)

    # Drop rows with missing values (or you can fill them)
    df = df.dropna()

    return df

def main():
    file_path = "youtube_2025_dataset_202504061614.csv"
    df = load_data(file_path)
    
    print("\n--- Original Dataset ---")
    print(df.head())

    clean_df = preprocess_data(df)

    print("\n--- Preprocessed Dataset ---")
    print(clean_df.head())

if __name__ == "__main__":
    main()
  
