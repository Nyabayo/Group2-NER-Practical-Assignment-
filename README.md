# Named Entity Recognition (NER) Model

This NER model utilizes the spaCy library to perform Named Entity Recognition on input text. It identifies entities such as persons, organizations, and locations within the provided text.

### Usage:
1. Ensure you have Python installed on your system.
2. Install the spaCy library using `pip install spacy`.
3. Download the English language model for spaCy by running `python -m spacy download en_core_web_sm`.
4. Copy and paste the provided code into a Python script or Jupyter Notebook.
5. Execute the script.
6. Input a sentence when prompted for NER testing.

### Example Usage:
```python
import spacy

def perform_ner(user_input):
    """
    Perform Named Entity Recognition (NER) on the provided user input using a pre-trained spaCy model.

    Args:
    user_input (str): A string of text provided by the user for NER.

    """
    # Load the pre-trained spaCy model
    nlp = spacy.load("en_core_web_sm")
    
    # Process the text
    doc = nlp(user_input)

    # Check if there are any entities detected
    if doc.ents:
        print("Recognized Entities:")
        for ent in doc.ents:
            print(f"{ent.text}: {ent.label_}")
    else:
        print("No entities detected in the input.")

# Prompt user for input
user_input = input("Enter a sentence for NER: ")
perform_ner(user_input)
```

### Test Inputs:
#### Example 1 :
"In 2021, the United Nations Climate Change Conference, also known as COP26, was held in Glasgow, Scotland, from October 31 to November 12. It was attended by world leaders including President Joe Biden of the United States, Prime Minister Boris Johnson of the United Kingdom, and Chancellor Angela Merkel of Germany, to discuss global efforts towards reducing carbon emissions and combating climate change."

#### Example 2 :
"Amazon, founded by Jeff Bezos in July 1994, started as an online bookstore but has since expanded into a wide array of other e-commerce products and services, including Amazon Web Services, one of the leading cloud computing services globally. Its headquarters is located in Seattle, Washington, and as of 2021, it is one of the world's highest-grossing online retailers."

#### Example 3 :
"The novel 'War and Peace' by Leo Tolstoy, published in 1869, is set during the Napoleonic Wars and offers a detailed narrative that explores the impact of these historical events on Russian society through the perspectives of five Russian aristocratic families. It is renowned for its complex characters and profound philosophical discussions on history and humanity."

#### Example 4 :
"On December 17, 1903, Orville and Wilbur Wright successfully conducted the world's first controlled, powered and sustained heavier-than-air human flight near Kitty Hawk, North Carolina. The Wright brothers' invention paved the way for the development of modern aviation, transforming transportation and military tactics in the 20th century."

Feel free to test the model with the provided inputs or any other text you wish to analyze for named entities.
Please leave a star and follow if you like the content
