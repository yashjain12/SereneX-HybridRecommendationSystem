Recommendation engines may use content-based and collaborative-based filtering methods. Each method has its pros and cons:

Collaborative filtering suffers from cold-start, which means when there is a new customer or item in the data, recommendation won’t be possible.
Content-based filtering tends to recommend similar items to that purchased/liked before, becoming repetitive. There is no personalization effect in this case.

In such cases, one may implement a hybrid recommendation system to address these issues.

Singular value decomposition is a linear algebra concept generally used as a dimensionality reduction method. It is also a type of matrix factorization. It works similarly in collaborative filtering, where a matrix with rows and columns as users and items is reduced further into latent feature matrixes. An error equation is minimized to get to the prediction.
A TF-IDF vectorization method for content based filtering:

$$\text{TF-IDF} = \frac{\text{Frequency of item}}{\text{Maximum Frequency of item}} \cdot \ln{\left(\frac{\text{Total Data}}{\text{Total Data with item}}\right)}$$

For the collaborative filtering model, SVD (singular value decomposition) is implemented. It is used to simplify and represent the movie data as a product of smaller matrices. If $A$ represents the larger dataset, then the SVD decomposition is $A = UEV^T$, but a low-rank approximation can be made by using submatrices of $U$, $E$, and $V^T$. If the storage of matrix $A$ requires $mn$ locations, submatrix $A_k$ of rank $k$ can be stored in only $(m+n)k$ locations, a huge computational improvement. Below is an image of this approximation:

![ss2](https://github.com/yashjain12/SereneX-HybridRecommendationSystem/assets/20261791/8255ef0f-ba82-4506-8d2b-a917128692e5)
