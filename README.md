# iMult-VAE

iMult-VAE



This Repository holds the notebooks which
we used to train our model, iMult-VAE.


Our model is variation  of variational autoencoders and collaborative
filtering, and is used to perform Top N predictions for songs recommendations,
which is a task in the field of Music Recommendation Systems.



Our model is based on the Mult-VAE model,
which was published in the paper
"Variational autoencoders for collaborative filtering" by Dawen Liang, Rahul G. Krishnan,
Matthew D. Hoffman, and Tony Jebara, in The Web Conference (aka WWW) 2018.



Our model differs in two ways from the original
paper:



·       
The
original paper uses only implicit user feedback to learn its weights, we
incorporate item-based side information to better tune the model’s weights. 



·     
Different
 selection: The authors of the original paper
describe a parameter named  which is used to control
the strength of regularization of the objective
function, the original paper performs a simple heuristic to
optimize the  value. We suggest to use  user-specific  values.


Dataset:



For the evaluation of our models, we used
the Million Song Dataset.



Specifically, we used two datasets from it:



The echo nest dataset 



This dataset contains (user id, song id,
play count) triplets for one million users.



This dataset was used as implicit user
feedback.



http://millionsongdataset.com/sites/default/files/challenge/train_triplets.txt.zip




 



The Last.FM Dataset



This dataset contains metadata for the
million songs in the MSD datset. 



This dataset was used as complementary side
information for the echo nest’s data. 



http://labrosa.ee.columbia.edu/millionsong/sites/default/files/AdditionalFiles/track_metadata.db
