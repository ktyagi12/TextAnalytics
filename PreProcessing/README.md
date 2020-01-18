# Text Pre Proccessing

**Text:** Any textual data from books, tweets, conversations between people, news, etc for mining, understanding, 
              representing what happens in physical and social world.
              
**Text Pre Processing:** The process to clean the raw text for further analysis without considering the context of the data.

**Text Pre Processing Steps:**
  1. Tokenisation and Normalization
  2. Stemming and Lemmatization (POS Tagging)
  3. Fixing the misspellings
  4. Stopword Removal
  5. Entity Extraction
  
**Steps:** 
1.  
  a. **Tokenisation:** The process of breaking down a corpus(large group) of texts into samller chunks like words or sentences.
  
  ![image](https://user-images.githubusercontent.com/38240162/72667806-a4194600-3a17-11ea-96df-a0bd3c103b90.png)
  
   b. **Normalization:** The process of transforming the text into a single canonical form. It is basically used to reduce the minor      differences between words with:
    I.  Accented Differences (apache, apaĆhe)
    II. Capitalize (the, The)
    III.Acronyms (U.S.A, USA)
    
  ![image](https://user-images.githubusercontent.com/38240162/72667908-be9fef00-3a18-11ea-8145-1725e3a28d07.png)
    
2. 
  a. **Stemming:** The process of reducing the inflections in words to their root form such as mapping a group of terms to their same stem even if stem is itself not a valid word. (Also called suffix stripping).
  
  ![image](https://user-images.githubusercontent.com/38240162/72668029-4c300e80-3a1a-11ea-9844-3118a1463c89.png)

  b. **Lemmatization:** The process of reducing the inflections in words to their root form ensuring that the resultant root words belongs to the dictionary. (Root word -> Lemma). It requires the input data should be POS-tagged.
    
   ![image](https://user-images.githubusercontent.com/38240162/72668147-91a10b80-3a1b-11ea-8d79-3b6d5809b81f.png)

    
  **POS Tagging:** It is a process of marking the words with their corresponding parts of speech based on both context and definition.
  
  ![image](https://user-images.githubusercontent.com/38240162/72668078-e3956180-3a1a-11ea-99f9-f6f52f8200ab.png)

  
3. **Fixing Misspellings:** The process of highlighting the incorrect spellings of tokens in corpus and correcting them by most close base word.
  
4. **Stopword Removal:** The process of removal of content less words which do not convey any meaning/context to the corpus.
  
  ![image](https://user-images.githubusercontent.com/38240162/72668192-1c820600-3a1c-11ea-945e-0fc5d6bbb799.png)

5. **Entity Extraction:** The process of identifying the conceptual identities behind the words rather than the dictionary knowledge.
   I.B.M -> IBM 
  

