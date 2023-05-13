# OpenAI Embeddings for Needs Clustering

This repository contains a Jupyter notebook that fetches and processes data from a CSV file, computes embeddings for data entries using OpenAI's API, and provides recommendations based on the closest matches (knn) found through these embeddings.

## Table of Contents

1. [Installation](#Installation)
2. [Environment Variables](#Environment-Variables)
3. [Data Format](#Data-Format)
4. [Usage](#Usage)
5. [Contributing](#Contributing)
6. [License](#License)

## Installation

To use this notebook, you'll need to install the following Python libraries:

- `openai`
- `python-dotenv`
- `pandas`
- `numpy`
- `tenacity`
- `pickle`
- `tiktoken`
- `nomic`

You can install these using pip:

```bash
pip install openai python-dotenv pandas numpy tenacity pickle5 tiktoken nomic openai-embeddings-utils
```

## Environment Variables

You'll need to set the following environment variables:

- `OPENAI_API_KEY`: Your OpenAI API key.

You can do this by creating a `.env` file in the root directory of this project and adding the following line:

```bash
OPENAI_API_KEY=your_openai_api_key
```

Replace `your_openai_api_key` with your actual OpenAI API key.

## Data Format

The data is expected to be in a CSV format file named `Problem_Intake_CurrentVers_TEST.csv` in the `source_data` directory.

The CSV file should have the following columns:
- `date`: The date of the data entry.
- `need`: The need statement.
- `contact`: The contact information.
- `dept`: The department associated with the need statement.

## Usage

To use the notebook, simply open it in your Jupyter notebook environment and run the cells sequentially. The notebook will:

1. Fetch data from the CSV file.
2. Compute the embeddings for each need statement using the OpenAI API.
3. Provide recommendations based on the closest matches found through these embeddings.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update the tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
