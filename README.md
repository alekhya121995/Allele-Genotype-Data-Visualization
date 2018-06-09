# Allele-Genotype-Data-Visualization
Scrapes data from CDC website, stores tables in a database and query it to visualize data

Introduction to the project

In this project, we look into NAT2, a gene with 5 variants. Variants in this gene (called
Polymorphisms) are closely linked with higher incidences of cancer and drug toxicity. In 
Korean patients, genetic polymorphisms of NAT2 and another gene CYP2E1 were
associated with toxicity in the liver when they were taking medication to treat tuberculosis.
rs1801280, rs1799930, and rs1801279 are three of the variants of NAT2. These variants
are slow acetylators, and having any of these variants versus the other three means that the
population is more sensitive to lower doses of TB treatment. Higher doses could lead to
toxicity.

The data from the CDC (Centers for Disease Control and Prevention) website organizes allele
and genotype percentages based on sex, ethnicity and race. Based on the percentages from
the tables, we can figure out which variant is most common for a particular group. The
website itself contains information for different genes and their variants. Linking the
percentage of each group to a disease can prove to be worthwhile to help in identifying
high risk groups.
 

Cleaning and Design Schema in SQL 

Each table scraped from the CDC was stored as its own variable and cleaned. 
Once the tables were created successfully, the next step was to design a schema to read
them in. All the tables were linked to the polymorphism table through variant, which was
the foreign key. The primary key for each table was a combination of variant and sex, age,
race or a combination of the two.
Each table was then stored in the relational database SQL for retrieval. Selecting a
relational database made most logical sense because all the tables were linked through
variant, which in turn belonged to one particular gene. 

Conclusion
In the future, this database can be made more useful by adding more of the genes from the
CDC and optimizing the entry. It can also be linked to epidemiology data to discover new
and interesting ways of predicting and diagnosing illnesses. Right now, the database can
return which variant is more common for a certain group and based on domain knowledge
we can link it to a disease. To make it more user friendly, all the required information can
be added to the database itself. Adding more races and expanding the database is also
something that can be done to make it more useful.
