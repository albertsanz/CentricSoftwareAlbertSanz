# CentricSoftwareAlbertSanz
Challenge solution for Centric Software
Readme file

## SQL Solution
```
select p.Title, i.Url, IFNULL(pd.TranslatedText, OriginalText) as ProductDescription
from product p left join ProductImages pi on p.Id = pi.ProductId
	 left join ProductDescription pd on p.Id = pd.ProductId
	 right join Image i on i.Id = pi.ImageId
where ImageIndex = 0 and pd.CountryCode = 'us';
```

## The Code's Perspective
The code developed for tackling steps 1 and 2 represents an initial solution but falls short of a full-fledged development in a real-world scenario. In practice, we would employ MLflow to facilitate model versioning during grid search, ensuring a more structured and manageable approach.

While Data Version Control (DVC) is a valuable tool for tracking dataset versions, its application wasn't deemed necessary in this instance, primarily due to a singular dataset version. Additionally, the exploratory data analysis (EDA) couldn't be conducted comprehensively due to time constraints.

In a real-world problem, a thorough examination of the model's performance across dataset labels would be imperative. For example, in the provided solution, we relied on upsampling alone to balance the dataset, as it was uncertain whether introducing downsampling might lead to underfitting or overfitting for certain labels.

It's important to note that while conducting these checks over the model and datasets is indeed crucial, they couldn't be performed in this instance due to significant time constraints. Nonetheless, in a production environment, where meticulous attention to detail is possible, these steps should be a priority.
