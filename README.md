# Group8-Bias

Codes belonging to the project "Topic 8- Where are the biases?" of the Deep learning for Natrual Language Processing course Sommer Semester 2022 at Bielefeld University.

Everything is in the Jupyter Notebook. All Functions are commented and can be used as they are described. For running the notebook file pathes and models as well as the tokenizers need to be adapted.

## Tokenizing the Data

    def tokenize_data(file_path,batch_size,tokenizer):

      """

      Function to split the data into test,training splits, tokenize and batch it.

      Input: Path fo the file, tokenizer

      Output: The tokenized and batched dataset

      """
  

## Group the tokens into batches of size b

     def group_texts(b):

        '''

        Function to put the tokenized data into batches

        Input: a batch, size controlled by the map function we use to call this function

        Output: 

        '''
  
## Finetunin a model
    def finetune_model(tokenizer,blocked_ds,base_model_name,model_name):

      """

      Function to finetune a model on our own dataset

      Input: tokenizer, tokenized data, name of the base model, name of finetuned model

      Output: Finished model which gets pushed to be hugging face hub (don't actually return it)

      """
  
  
 ## Evaluate finetuned model and templates with class LanguageModelEvaluator() 
 
    def evaluation(model_name,tokenizer,file_path,choices):

      """

      Function to evaluate the templates

      Input: model and tokenizer name, the tokenizer, file path to the template, choices (i.e. which words could be used for the empty place)

      Output:

      """
  
    class LanguageModelEvaluator():

      """

      Class to evaluate the templates

      Input: templates, choices, model and tokenizer

      Output: Dataframe of the templates, which word would be used to fill the empty space, which words the model would use itself

      """

  
 ## Evaluate bias of a model. 
 
    def evaluate_bias(model,tokenizer,targets,csv_file):

      """

      Function to evaluate bias in a model

      input: model,tokenizer,list of tagets, path to csv file with templates and attributes

      output: DataFrame with log normalized proabbility,probability, prior and scaled probability of sentences,targets and attributes

      """

 
    def cohend(d1, d2):

      """

      Function to calculate cohens d

      """
  
  
    def calc_bias(df):

      """

      Function to calculate cohens d or the categorical bias depending on targets: if two targets cohens d otherwise CB

      Input: dataframe calculated above

      Output: cohens d or cb score

      """  
  
    def calc_jsd(df):

      """

      Function to calculate the JS Divergence between pairs of targets

      """
  
