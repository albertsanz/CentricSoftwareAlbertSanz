# CentricSoftwareAlbertSanz
Challenge solution for Centric Software
Readme file

SQL Solution
```
select p.Title, i.Url, IFNULL(pd.TranslatedText, OriginalText) as ProductDescription
from product p left join ProductImages pi on p.Id = pi.ProductId
	 left join ProductDescription pd on p.Id = pd.ProductId
	 right join Image i on i.Id = pi.ImageId
where ImageIndex = 0 and pd.CountryCode = 'us';
```

About the code

The developed code to solve steps 1 and 2 it's not considered a solution for a real development. 
In a real case, I would have applied MLFlow over the gridsearch to persist the model versioning. 
Also, I could have used of DVC ( data version control), but in this case, as there is only one dataset version, it hasn't been considered to apply DVC.
Furthermore, the EDA has not been deeply study due to the lack of time. 
In a real case problem, I would have been studied the model limits over the dataset labels. 
For instance, in the provided solution, only upsampling is applied to balance the dataset, because of the unknowing if by also applying downsampling the model will have underfitting or overfitting for some labels.
Moreover, it hasn't been tested, at all, the model response over leaving the dataset slighty unbalanced and compare it with the fully balanced one.
