
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Examining the relationship between race and food insecurity in Texas, U.S.

<!-- badges: start -->
<!-- badges: end -->

Amanda Rorat (400437934)  
Emma Bilbija (400310926)  
Mackenzie St. Arnault (400373298)  
Nicole Santos (400330468)  
Nolyn Lakhanpal (200008359)  
Thea Chu (400307018)

Final project for [ENVSOCTY 4GA3 Applied Spatial
Statistics](https://academiccalendars.romcmaster.ca/preview_course_nopop.php?catoid=53&coid=267722)
(McMaster University)

## Abstract

This paper reports an analysis of food insecurity in Texas, USA, and its
relationship with race. The analysis was carried out at the tract level.
Data were obtained from the US Census.

# Introduction

Approximately 18 million households experienced food insecurity at some
point in 2023, with almost 7 million facing very low food insecurity
(USDA, 2025). This makes up 13.5% of the total households in the United
States of America, an increase of approximately one million households
from 2022. Texas holds the second-highest rate of all states. 16.9% of
Texas households face food insecurity in 2023 (USDA, 2025). This means
that 16.9% of households went without access to nutritious and safe
foods at some time in 2023. Caring about the impact that race has on
food insecurity is crucial, as it highlights the systemic inequalities
within marginalized communities. To understand this issue and strive for
a state with adequate food for all residents, further understanding of
the problem is needed.  
Additionally, studies have shown that access to food is impacted by race
(Beaulac et al., 2009). This paper aims to examine the relationship
between race and food insecurity in the state of Texas, U.S., using food
stamp usage as a proxy measure for food insecurity. The goal is to
understand the relationship between these variables and why this
phenomenon may occur. By the end of this paper, a better understanding
of the overarching topic of racial disparities in food insecurity,
specifically in Texas, will be found.

Three research questions guide the analysis in this paper:  
  
(1) How do race and food stamp usage vary across Texas counties?  
  
(2) Are there any clusters of food insecurity, and do these clusters
correlate with racial composition?  
  
(3) Does racial composition predict food insecurity after accounting for
socioeconomic factors and other confounders, and does this relationship
vary geographically?  
  
Our report will cover three primary sections:

## Descriptive Statistics

The first section of analysis will analyze the basic patterns of race
and food stamp usage, calculating descriptive statistics for both
variables to address the first research question. The results of this
section are summarized in tables of descriptive statistics. Choropleth
maps are used to visualize the spatial trends in this data. This section
identifies the baseline geographic patterns of food insecurity and
racial composition.

## Spatial Statistics

Next, to address research question two, food insecurity and racial
composition will be tested to identify any clustering or distribution.
These are methods of spatial autocorrelation. Food stamp usage hotspots
are tested for overlap with clusters of certain racial groups.

## Inferential Statistics

The final analysis section uses OLS regression models to control for
confounding variables such as income or education. Regression analysis
will reveal the extent to which race plays a role in predicting food
insecurity, independent of any possible confounders in order to address
the third research question. Methods of geographically weighted
regression models are used to better understand the role of geography in
shaping this relationship.

# Background

## Defining Food Insecurity

Food insecurity refers to the lack of reliable access to sufficient,
nutritious food which encompasses four dimensions: availability, access,
stability and utilization (Uppal, 2023). Insecure household may face
difficulties in acquiring food, affording nutritious meals or maintain
stable access due to infrastructure or economic disruption. According to
the USDA, food insecurity can range from limited dietary variety and
quality to severe disruptions like insufficient food intake
(Coleman-Jensen et al., 2019). Beyond nutritional concerns, it is
closely linked to a higher likelihood of chronic illnesses, mental
health issues, frequent hospital visits and even mortality (Uppal,
2023). In 2018, around 11.1% of households in the United States, over 14
million, struggle with food insecurity, including 4.3% that experienced
very low food security (Coleman-Jensen et al., 2019). On a global scale,
rates of food insecurity have been increasing, driven by factors of
inflation, economic uncertainty, and systemic inequalities. While these
national statistics are alarming, Texas often exceeds national averages,
particularly in marginalized and rural areas. In 2020-2022, 15.5% of
households were food insecure, exceeding the national average of 12.8%
(USDA ERS, 2023). Therefore, highlighting its urgency as a case study
for deeper spatial and racial food access disparities (Dean & Sharkey,
20100; Janda et al., 2022). The complex and multifaceted nature of food
insecurity calls for both large-scale policy reforms and locally
tailored, community-driven strategies.

## Structural Causes of Food Insecurity

Food insecurity is associated with various structural inequalities,
including income disparities, access to capital, and systemic barriers
rooted in racism. Several studies revealed that food insecurity is the
result of compounding factors that disproportionately affect racialized
communities in the United States. In a systematic review of studies on
food deserts by Beaulac et al. (2009), they concluded that socioeconomic
deprivation at the community level intensifies individual-level
disparities in the United States. Their review concluded that low-income
neighbourhoods that were predominantly African American continuously had
fewer supermarkets while experiencing limited geographic access to
affordable, healthy food (Beaulac et al., 2009). This structural
disadvantage hinders an entire community’s access to nutritious foods,
especially in areas dominated by convenience stores that typically offer
unhealthy and expensive food items.

Similarly, Myers and Painter (2017) examined the relationship between
race/ethnicity, nativity and food insecurity. They found that Black and
Latino households in the United States suffer more than twice as much
from food insecurity in comparison to white households, even when
accounting for socioeconomic status (Myers & Painter, 2017). Given that
minority neighbourhoods have fewer quality supermarkets regardless of
socioeconomic status, the authors suggest this gap stems from spatial
inequalities. These spatial inequalities indicate that race, independent
of income, shapes access to nutritious food. Nam et al. (2015) confirm
these findings in their analysis of racial disparities in food
insufficiency. In their study, the authors found that Black, Hispanic,
and American Indian families experience food insecurity at a
statistically significantly higher rate than White families (Nam et al.,
2015). When the authors conducted a breakdown of contributing factors,
they discovered that this disparity among the minority groups was tied
mainly to lower home ownership rates, access to credit, and insufficient
financial assets (Nam et al., 2015). These economic disparities increase
susceptibility during times of financial hardship, restricting minority
families’ ability to protect themselves from food insecurity.
Collectively, the research conducted emphasizes that the intersection of
race and socioeconomic class creates compounded disadvantages for
families of non-White backgrounds. Furthermore, this suggests that food
insecurity in the United States, particularly in Texas, is not solely
tied to income but several other systemic barriers that are shaped by
racial inequality.

## Race, Place, and Access

Texas food insecurity is deeply shaped by spatial and racial
inequalities in food access. In rural Central Texas, residents often
face limited access to supermarkets and healthy food outlets, typically
traveling long distances for groceries and relying on nearby convenience
stores with fewer nutritious options. This geographic isolation, coupled
with underdeveloped infrastructure and lack of public transportation,
contributes to higher food prices and limited dietary quality compared
to urban areas (Dean & Sharkey, n.d.; Dean & Sharkey, 2011). Janda et
al. (2022) further support these findings, examining food insecurities
across different geographic contexts in Travis County. They found that
individuals living in rural zip codes were more than twice as likely to
experience food insecurities compared to those in urban areas. This
remains significant even after controlling for factors like income,
educational level, employment status and access to transportation (Janda
et al., 2022). Additionally, Janda’s 2020 dissertation research
documented rural and peri-urban callers to the 2-1-1 helpline in Central
Texas. The finding shows that these areas were significantly more likely
to seek help with food assistance. This was true for individuals living
in zip codes that lacked supermarkets, emphasizing the role that
geographic proximity plays in shaping spatial disparities in food
access.

Race and geography shape disparities in food insecurity across Texas.
The Supplemental Nutrition Assistance Program (SNAP), formerly known as
food stamps, was established to combat food insecurity among low-income
populations providing assistance to purchase food.Yet disparities
persist even among SNAP-eligible households. Samuel et al. (2023) found
that across the United States, SNAP-eligible Black and multiracial
households experience higher rates of food insecurities compared to
White counterparts. This disparity was especially evident among those
who were not enrolled in the program. Among households not participating
in SNAP, those that identify entirely Black were 52% more likely to
experience food insecurity compared to White households. Similarly,
multiracial households faced a 42% higher risk of food insecurity than
their White counterparts. Importantly, among households actively
participating in SNAP, the racial disparities in food insecurity were no
longer observed. This suggests that while food assistance programs can
help reduce the effects of structural inequalities, it does not entirely
eliminate them (Samuel et al., 2023). In Central Texas, Janda et
al. (2022) reported that Hispanic participants had 2.79 times greater
odds of being food insecure than participants who were non-Hispanic
white. This aligns with the broader finding identifying that
race/ethnicity often intersect with income in shaping food insecurity
risk (Janda et al., 2022). Janda and others highlight that communities
of color are disproportionately affected by systemic barriers such as
reduced access to full-service grocery stores and over reliance on small
retailers with fewer healthy options (Beaulac et al., 2009; Walker et
al., 2010; Janda et al., 2022).

Rural Texans face unique and persistent barriers to food security, often
shaped by limited infrastructure, social isolation and inadequate food
retail presence. Dean and Sharkey (2011) emphasized that rural areas not
only lack supermarkets, but exhibit weaker social networks and less
communal support. These factors further undermine resilience against
food insecurity. Janda et al. (2022) extends on this understanding by
showing that rural residents in Central Texas often live farther from
supermarkets, an average of 1.66 miles but closer to convenience stores
with an average of 0.67 miles. This proximity gap disproportionately
affects low-income and Hispanic households, exacerbating nutritional
disparities and increasing vulnerability to food insecurity (Janda et
al., 2022).

Moreover, the uneven distribution of food retailers and limited
transportation options in rural areas indicate that effective solutions
must be customized to local needs and the resident’s lived experiences.
Janda et al. (2022), emphasize the importance of incorporating factors
such as perceived accessibility, community preferences and cultural
appropriateness. These factors are often overlooked in conventional
approaches to identify food deserts.

## Policy Landscape and Limitations

SNAP (formerly known as food stamps) is the largest federal food
assistance initiative in the United States. It is designed to alleviate
food insecurity by providing financial support for low-income families.
While SNAP reduces food insecurity by helping millions of families each
year, its effectiveness is still limited by structural and environmental
factors. Grummon and Taillie (2018) found that even with SNAP
participation, there are still racial disparities in purchasing
patterns. Their findings show that Black SNAP participants tended to
purchase more processed meats, sweeteners, and low-nutrient foods
compared to White participants of the program (Grummon & Taillie, 2018).
Notably, these disparities do not appear in non-participating families.
This suggests that the SNAP program, although it may aid in access to
food, does not enhance diet quality equally among different
racial/ethnic groups (Grummon & Taillie, 2018).

Odoms-Young (2018) highlights how these disparities are influenced by
structural racism in food systems and public policy. Factors such as
housing segregation, financial inequality, and high incarceration rates
disproportionately impact communities of colour (Odoms-Young, 2018).
These factors create barriers to food assistance and healthy food
options. The author also notes that these racial disparities exist even
when socioeconomic factors are removed (Odoms-Young, 2018), highlighting
once again that race independently impacts access to nutritious foods.

A study of a low-income Latino neighbourhood in Upstate New York by
Lopez-Class and Hosler (2010) revealed that most local stores that
accepted SNAP still provided limited access to nutritious items and high
food prices. For example, only one store in the entire neighbourhood
carried high-fiber bread compared to seven in the adjacent non-Latino
neighbourhood (Lopez-Class & Hosler, 2010). On top of this, many of the
stores were not disability-accessible and public transport to these
locations was insufficient (Lopez-Class & Hosler, 2010). Consequently,
residents without cars were often forced to rely on smaller retailers
with higher prices and fewer nutritional options, which erodes the
intended support of SNAP assistance (Lopez-Class & Hosler, 2010).

In conclusion, while SNAP has been critical for tackling food
insecurity, its current system fails to address the disparities in
purchasing patterns of minority groups and the system issues that lead
to these racial and geographic disparities. Effective policy reforms are
required to consider inequitable food access caused by transportation
limitations, and racial and place-based disparities that constrain how
SNAP assistance is used.

## Gaps in the Literature

Despite substantial research on food insecurity in the United States,
particularly in Texas, a significant gap remains. The gaps are seen in
studies that integrate both spatial and racial/ethnic dimensions using
spatially explicit methods. Most of the existing studies focus on racial
disparities (e.g. food insecurity among Black, Latino and immigrant
community) or spatial disparities (e.g. rural-urban food deserts) but
rarely examine how race, place and poverty interact at a localized scale
(Beaulac et al., 2009; Myers & Painter, 2017). Myers and Painter (2017)
found persistent food insecurity divide across racial/ethnic and
nativity lines, even after controlling for socioeconomic status. On the
other hand, spatial studies like Janda et al. (2022) and Lopez-Class &
Hosler (2010) underscore geographic barriers like proximity to
supermarkets but does not consistently take into account for racialized
experiences of those affected. Furthermore, studies examining the impact
on SNAP on reducing disparities have primary used cross-sectional or
nationwide datasets. This often fails to capture how SNAP participation
intersect with race and geographical context at a local level (Grummon &
Taillie, 2018). This leaves an analytically blind spot regarding
localized, intersectional factors of food insecurity in Texas. This
project hopefully contributed to closing this gap by using inferential
and spatial statistical methods to examine how race, income, location
and SNAP usage interact, offering a greater understanding of food access
inequalities in Texas.

# Study area

Food insecurity was studied at the tract level in the state of Texas
(see Figure 1). There are 6896 tracts in the state, and each of these
tracts was used in the analysis. In the U.S., around 11.1% of households
experience food insecurity. Texas faces higher rates, with 14% of
families identifying as food insecure in 2018 (Coleman-Jensen et
al. 2019). The state was selected for this reason, having a higher rate
of food insecurity in the country. Many studies conducted in Texas have
detailed the relationship between food insecurity and other variables. A
study by Beaulac et al. (2009) found that food access in the U.S. is
significantly impacted by income and race. This study was conducted to
analyze the spatial patterns between these variables and discuss the
potential reasons for them.

![](README_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

# Data

The data used for the project primarily comes from the U.S. Census
Bureau. This data can easily be imported into R using the “tidycensus”
package. Additionally, the “tidyverse” package will be used since it
contains key libraries such as “ggplot2” which will allow us to plot the
census data for each county within Texas, making any spatial patterns
easily identifiable. The full list of packages included within the
tidyverse is available on their website. The “sf” package for Simple
Features will also be imported to make spatial data easier to create and
visualize. Likewise, we will use packages such as “gt” and “kableExtra”
to create clean looking tables.

Listed below are the U.S. Census Bureau variables used with their
respective R codes (that allow us to import the data directly into R
through the tidycensus package). The data used will be from 2023 which
is the most recent year in which the data is available in R.  
  
![Data Sources](figures/Data_Table.png)  
The food stamp count is crucial to use to identify food security or
insecurity in each county, as that is the most relevant quantitative
data relating to food security that we could find. By converting food
stamp usage to per capita rates (using the population for each county),
the similarities and/or differences in food stamp usage (and
consequently, food security/insecurity) can be mapped using ggplot2.
This can then be compared to racial demographics (mapped by comparing
the white, black, Asian, American Indian and to see if there is a
potential correlation between race and food insecurity/food stamp usage.

# Methods

## Methods for Descriptive & Spatial Statistics

County-level data on food stamp usage and race in Texas were analyzed
using the df_race.rds shapefile. This shapefile included variables such
as the percentage of residents receiving food stamps and racial
composition. It was imported into R and reprojected using st_transform()
to EPSG:3857 to ensure accurate distance-based and spatial relationship
calculations.

To visualize the geographic distribution of food stamp usage, an initial
choropleth map was created using ggplot() and geom_sf(), with the
variable food_stamp_p representing the percentage of food stamp
recipients in each county. The scale_fill_viridis_c() was used to apply
a colour gradient that improves interpretability for viewers by
emphasizing variation in values. Prior to analysis, counties with
missing values were excluded using filter(!is.na(food_stamp_p)) to
prevent skewed results and ensure clean spatial computations.

To analyze local spatial interactions, a neighbourhood structure was
established using Queen contiguity through the poly2nb() function, which
identifies counties as neighbours if they share a boundary or a corner
point. This structure was then transformed into a spatial weights matrix
using nb2listw(), allowing the influence of neighbouring counties to be
incorporated into subsequent spatial analyses.

Spatial moving averages (SMAs) were computed using lag.listw() for key
variables such as food stamp usage (sma_food_stamp_p) and racial
proportions (e.g., sma_white_p, sma_black_p, sma_asian_p,
sma_american_indian_p, sma_pacific_islander_p, sma_other_p). SMAs
provide a smoothed view of regional patterns by averaging the values of
surrounding counties instead of the raw data. This approach emphasizes
clusters of consistent low or high values, making the broader spatial
trend easy to identify.

A null simulation envelope was generated to assess whether observed
spatial patterns were stronger than would be expected under random
distribution. It involved randomizing the food stamp usage values using
a sample (food_stamp_p) and recalculating the SMA of the randomized
data. Therefore, it created a baseline scenario representing spatial
randomness, allowing for visual and statistical comparison with the
actual SMA pattern. The difference between the observed and randomized
results offers insight into the presence and strength of spatial
autocorrelation within the data.

The local Gi\* statistic (Local G) was computed using localG() from the
spdep package to identify areas of statistically significant clustering.
This technique evaluates each county’s value relative to the average of
its neighbouring counties and generates a Z-score. This Z-score
determines whether it belongs to a statistically significant high-value
cluster (hotspot) or a low-value cluster (coldspot). The analysis was
applied to food stamp usage and racial proportion to explore the spatial
overlap between race and food insecurity. The resulting Gi\* values were
incorporated using mutate() and converted to numeric format using
as.numeric() to enable plotting. Since localG() outputs a specialized
object class, converting the results to numeric format was required to
ensure compatibility with ggplot() for mapping and visualization.

Lastly, maps were generated to visualize the Gi\* Z-scores using
ggplot() and scale_fill_gradient2(), with a midpoint of zero. Red tones
indicated statistically significant hotspots (high-value clusters),
blue/green tones indicated coldspots (low-value clusters), and yellow
areas represented neutral or non-significant regions. This mapping
approach successfully highlighted clusters of food insecurity and racial
distribution, offering a spatial perspective for understanding systemic
disparities among the counties in Texas.

## Methods for Regression Analysis

Regression models were estimated using tract-level data on per-capita
food stamp usage, racial composition, and several control variables,
including unemployment rate, median household income, and per-capita
households with children.

Initial analyses employed methods of Ordinary Least Squares (OLS)
regression to examine the relationship between food stamp usage and
racial composition, controlling for socioeconomic factors. To resolve
the challenge of perfect multicollinearity, the White racial category
was omitted as the reference group. Both linear and log-transformed
models were tested to explore differences in functional form. However, a
Moran’s I test using the moran.test() function revealed significant
spatial dependence, prompting further investigation.

To address spatial autocorrelation in the OLS residuals, a spatial
weights matrix was constructed using a k-nearest neighbors approach.
Tract centroids were calculated using st_centroid(), and neighborhoods
were defined with k=4 using knearneigh(). The final spatial weights
matrix was constructed using nb2listw().A geographically weighted
regression (GWR) model with Gaussian weighting was then estimated using
gwr.sel() and gwr() to produce localized estimates. However, residuals
from the GWR model remained spatially autocorrelated, as indicated by a
Moran’s I test.

To explicitly account for residual spatial dependence, a Spatial Error
Model (SEM) was estimated. This method accounts for spatial
autocorrelation by incorporating a function of the spatially dependent
residuals within the error term. A Moran’s I test confirmed spatial
independence of the SEM residuals, indicating the validity of the
estimates.

# Analysis

## Descriptive Statistics

![](README_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

## Spatial Statistics

### Chloropleth Visualization of Food Stamp Usage in Texas

![](README_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

### Spatial Moving Averages

![](README_files/figure-gfm/unnamed-chunk-17-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-18-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-20-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-21-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-22-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-23-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-24-1.png)<!-- -->

The Spatial Moving Average (SMA) map for food stamp usage reveals a
clear spatial clustering pattern, particularly concentrated in the
southern and southwestern regions of Texas. These clusters are
characterized by darker shading, indicating that high food stamp usage
is not randomly distributed but spatially grouped. This visual pattern
is further supported when compared to the randomized null SMA map, which
lacks any coherent structure or concentration, reinforcing the idea that
the observed clustering is meaningful rather than due to chance. When
the food stamp map is visually compared to the SMA maps for racial
demographics, some alignment emerges, but the degree of overlap varies
across groups. For example, the Black population displays strong
clustering in the eastern part of the state, where there is also notable
food stamp usage, suggesting a potential spatial relationship. The white
population is more heavily clustered in central and northwestern Texas,
with only partial overlap in the southwest, where some food stamp
clustering also appears. Other racial groups, including Asian, American
Indian, Pacific Islander, and those categorized as “Other” show more
dispersed or minimal clustering, making spatial comparisons less
conclusive. Overall, while visual analysis of the SMA maps highlights
several potential co-located clusters, especially for the Black
population, these observations remain exploratory. The spatial
clustering suggests areas of concentrated socio-economic vulnerability,
but the strength of the relationship between race and food stamp usage
would require more rigorous statistical testing to confirm.

### Local G

![](README_files/figure-gfm/unnamed-chunk-26-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-28-1.png)<!-- -->

### Gi\* for Each Race

![](README_files/figure-gfm/unnamed-chunk-30-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-31-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-32-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-33-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-34-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-35-1.png)<!-- -->

The Gi\* analysis reveals statistically significant spatial clustering
in food stamp usage and racial group distributions across Texas. For
food stamp usage, there are strong hotspots (red) in the southwestern
and southern parts of the state, indicating counties where food stamp
reliance is significantly higher than expected. This hotspot regions are
especially seen in the southern border like Rio Grande Valley,
reflecting socio-economic challenges faced in that region. A null
landscape of food stamps usage was created and confirmed with mapping
that these clustered are statistically significant and not random. It
highlighted how poverty is geographically concentrated in historically
marginalized areas. When examining the racial distribution, distinct
spatial patterns were een. Areas with lower White population densities
(coldspots) largely overlap with food stamp usage hotspots. It suggest
that food insecurity is more prevalent in counties of Texas with higher
proportion of non-White residents. Meanwhile, Asian population hotspots
are tightly clustered around urban areas like Houston or Dallas. There
is some overlap in these areas with high food stamp usage. It suggest
that the Asian community have a better socioeconomic condition in
comparison to the others. The American Indian population shows a
moderate and localized clustering of Indigenous population. The clusters
are seen as rural west and central Texas. Some American Indian hotspots
coincide with regions of higher food insecurity, suggesting that rural
Indigenous communities face more greater challenges. As they are more
isolated geographically and have limited economic opportunities in
comparison to the others. However, the clustering is less intense and
continuous in compared to the other racial groups. These results reflect
a more smaller and more disperse population of American Indian across
the region of Texas. The Black population, the hotspots are concentrated
east of Texas and major urban centers and shows a great amount of
overlap with food stamp usage. This spatial pattern reveals the enduring
impact of historical racial segregation and economic marginalization. On
the other hand, Pacific Island population hotspots are more isolated and
scattered. This is may be likely due to relatively small population
numbers. Lastly the other racial category, likely capture multiracial
and diverse ethnic groups. This “Other” racial category forms strong
hotspots in west Texas and aligns with food stamp hotpots. It suggest
that those that are racially diverse population may experience
heightened economic vulnerability. Overall these results show that food
insecurity in Texas is not evenly distributed and is tied to racial and
geographic factors. Minority and marginalized racial groups are likely
to be concentrated in regions with persistent poverty. While certain
urban population experience stability. The geographic overlap between
racial demographics and food insecurity highlights deeper systemic
inequalities, emphasizing the importance of implementing social and
economic policies that account for both racial and regional differences.

## Regression Analyses

### Spatial Error Model

A Spatial Error Model was employed to account for residual spatial
dependence. The results for this specification are outlined in the table
below:

<figure>
<img src="figures/screenshot.png" alt="regression" />
<figcaption aria-hidden="true">regression</figcaption>
</figure>

The Spatial Error Model (SEM) reveals statistically significant
relationships between food stamp usage and racial composition across
Texas census tracts. Because the per capita proportions for all race
groups must sum to 1.00, the White race category was excluded from the
regression to avoid multicollinearity. Therefore, “White” serves as the
reference group.

Holding all other variables constant, a one percent increase in the
share of Black residents corresponds to a 0.057% rise in per capita food
stamp usage (p \< 0.0001), while a one percent increase in the “other”
category yields a 0.037% increase (p \< 0.0001). In contrast, a one
percent uptick in the Asian share leads to a 0.018% decrease in food
stamp usage (p $\approx$ 0.007). The American Indian and Pacific
Islander coefficients are not statistically significant at the 10% level
(p = 0.603 and p = 0.198, respectively).

Among the control variables, every additional \$10,000 in median
household income predicts about a 0.006% decrease in per capita food
stamp usage (p \< 0.0001). On the other hand, higher values in
per-capita households with children and unemployment rate increase
reliance on food stamps by 0.197% and 0.133% respectively (both p \<
0.0001).

The SEM’s spatial error coefficient is $\lambda$ = 0.53 (p \< 0.001),
indicating substantial spatial clustering in the regression errors. This
high lambda value justifies our use of the SEM specification. Indeed,
the SEM outperforms OLS with a much lower AIC (–26,092 vs. –24,818).

### Tests for Spatial Indepedence

To confirm that we’ve successfully removed residual spatial
autocorrelation in the SEM specification, a Moran’s I test on the
residuals was employed.The result of Moran’s I = –0.0396 (p \< 0.0001)
reveals a slight negative autocorrelation that is highly significant.
This demonstrates that the SEM specification has successfully absorbed
spatial dependence in the residuals, thus validating the reliability of
our regression coefficients. These results are illustrated below, with
the Morans I test and a map of the spatially independent residuals.

    Moran I test under randomisation

data: model.sem1\$residuals  
weights: df_race_c.w

Moran I statistic standard deviate = -4.947, p-value = 3.769e-07
alternative hypothesis: less sample estimates: Moran I statistic
Expectation Variance -3.960006e-02 -1.471670e-04 6.360299e-05

<figure>
<img src="figures/sem_r_map.png" alt="Sem Map Res" />
<figcaption aria-hidden="true">Sem Map Res</figcaption>
</figure>

Together, these results reveal a strong relationship between race and
food stamp usage across Texas census tracts. Relative to the White
population (which serves as the reference group), areas with a higher
proportion of Black residents show the largest increase in food stamp
usage. Therefore, communities with a high percentage of Black residents
experience a disproportionately larger reliance on SNAP compared to any
other race group. Similarly, tracts with a greater share of residents
classified in the “other” racial category also show higher food stamp
usage than White census tracts, though this relationship is slightly
weaker than it is for Black communities. In contrast, tracts with a
greater proportion of Asian residents actually show lower food stamp
usage compared to White tracts. The coefficients for American Indian and
Pacific Islander groups are not statistically significant, and so these
coefficients are not directly interpretable. Additionally, the control
variables follow expected patterns. A higher median household income is
associated with lower food stamp use, while greater unemployment and a
greater share of households with children correspond with increased food
stamp usage.

# Conclusion

Throughout the use of different inferential and spatial statistical
methods, patterns of food access inequalities within counties of Texas
were revealed relationships between race, income, location, and SNAP
usage. There are clear patterns of spatial autocorrelation, which
suggest that high food stamp usage is prevalent in the southern areas of
Texas, shown by the clustering pattern portrayed in the map for the
spatial moving average and the Gi\* plot. This clustering supports the
conclusion that the use of food stamps in Texas counties is not random.
Additionally, when comparing SMA maps between food stamp usage and
racial groups, some co-location patterns emerge. For example, Black
population SMA hotspots often overlap with areas of high food stamp
usage, especially in eastern Texas. This spatial relationship suggests
that Black-majority counties may be more vulnerable to food insecurity.
Meanwhile, the white population is concentrated in central and
northwestern regions, which tend to show lower food stamp usage,
highlighting a potential spatial divide between majority-white counties
and areas facing economic vulnerability.

The clustering patterns may suggest that regions with high food stamp
usage also have high concentrations of specific racial groups, which can
lead to structural and system inequalities within the community. Results
from the Gi\* hotspot analysis further confirmed this. Statistically
significant Gi\* hotspots for food stamp usage were observed in Texas’s
southern and southwestern border regions, most notably along the Rio
Grande Valley. Many of these hotspots overlap with areas of lower white
population density and higher concentrations of racially diverse
communities, particularly those identified as Black, “Other,” and
American Indian. The Black population displayed strong hotspots in the
east, including urban centers, indicating persistent historical
inequities and segregation. The Asian population showed a unique
clustering pattern, concentrated around urban centers like Houston and
Dallas, with comparatively lower food stamp usage. This pattern may
reflect more stable socioeconomic conditions among some Asian
communities in urban areas. In contrast, the Pacific Islander and
“Other” groups had scattered or localized clusters that also intersected
with food insecurity zones, suggesting more complex or underrepresented
vulnerabilities.

These spatial trends are further supported by the regression analysis,
which confirms that race remains a statistically significant predictor
of food stamp usage even after controlling for income, unemployment, and
household composition. Tracts with higher shares of Black and “Other”
populations were significantly more likely to report increased food
stamp reliance, while Asian-majority tracts were associated with lower
usage relative to the White reference group.

Together, these findings support the study’s original research questions
and reinforce key themes from the background literature. First, there is
substantial variation in food stamp usage across counties, driven in
part by racial composition. Second, statistically significant spatial
clusters exist for food insecurity and racial demographics, and their
co-location provides strong visual and analytical evidence of structural
disparities. Lastly, spatial analysis confirms that food insecurity in
Texas is patterned by more than just income or geography, and that race
plays a significant role even after accounting for other factors, as
further supported by regression analysis in later sections.

## Recommendations

To build on the findings of this study, further research should
investigate how intersecting factors such as race, geographic location,
and socioeconomic status compound food insecurity risk. While this study
relied on proxies such as food stamp usage and racial composition,
future work could incorporate finer-grained data (e.g., food access
infrastructure, program enrollment barriers, transportation
availability) to capture better the lived experience of food insecurity
in Texas communities. Additional spatial methods, including spatial lag
or geographically weighted regression at finer scales, would further
clarify causal pathways and regional variability.

From a policy standpoint, spatially targeted food access interventions
should prioritize the hotspot regions identified in this study.
Particular areas of concern are southern and eastern counties where food
stamp usage and racialized disadvantage are highly concentrated. These
are not just areas of economic deprivation, but zones where structural
inequalities have persisted. Programs like SNAP should also be evaluated
on factors such as spatial accessibility, diet quality, and equitable
outcomes across racial groups. Expanding mobile grocery services,
incentivizing supermarkets in underserved areas, and increasing
culturally relevant outreach could address access barriers specific to
Black, Indigenous, and racially diverse populations. Policy must move
beyond income-based thresholds to recognize the spatial and racial
dimensions of food insecurity that our findings reveal.

# References

<!-- Hanging indent block -->

<div style="margin-left: 0.5in; text-indent: -0.5in; line-height: 1.5;">

Beaulac, J., Kristjansson, E., & Cummins, S. (2009). A systematic review
of food deserts, 1966–2007. *Prevention of Chronic Disease, 6*, A105.
<https://resolver-scholarsportal-info.libaccess.lib.mcmaster.ca/resolve/15451151/v06i0003/nfp_asrofd1.xml>  
  
Coleman-Jensen, A., Rabbitt, M. P., Gregory, C. A., & Singh, A. (2019).
*Household Food Security in the United States in 2018 (Economic Research
Report Number 270)*. <https://doi.org/10.22004/ag.econ.301167>  
  
Dean, W. R., & Sharkey, J. R. (2011a). Food insecurity, social capital
and perceived personal disparity in a predominantly rural region of
Texas: An individual-level analysis. *Social Science & Medicine, 72(9)*,
1454–1462. <https://doi.org/10.1016/j.socscimed.2011.03.015>  
  
Dean, W. R., & Sharkey, J. R. (2011b). Rural and urban differences in
the associations between characteristics of the community food
environment and fruit and vegetable intake. *Journal of Nutrition
Education and Behavior, 43(6)*, 426–433.
<https://doi.org/10.1016/j.jneb.2010.07.001>  
  
Government of Canada, S. C. (2023, November 14). *Food insecurity among
Canadian families*.
<https://www150.statcan.gc.ca/n1/pub/75-006-x/2023001/article/00013-eng.htm>  
  
Grummon, A. H., & Taillie, L. S. (2018). Supplemental Nutrition
Assistance Program participation and racial/ethnic disparities in food
and beverage purchases. *Public Health Nutrition, 21(18)*, 3377–3385.
<https://doi.org/10.1017/S1368980018002598>  
  
Hernandez, D. C., Reesor, L. M., & Murillo, R. (2017). Food insecurity
and adult overweight/obesity: Gender and race/ethnic disparities.
*Appetite, 117*, 373–378.
<https://doi.org/10.1016/j.appet.2017.07.010>  
  
Janda, K. (2020). *A Geospatial Examination Of The Association Between
Geographic Food Access And Food Insecurity In Central Texas: The Role Of
Race/Ethnicity And Urbanicity* \[Master’s thesis, UTHealth School of
Public Health\]. Dissertations & Theses (Open Access).
<https://digitalcommons.library.tmc.edu/uthsph_dissertsopen/134>  
  
Janda, K. M., Ranjit, N., Salvo, D., Hoelscher, D. M., Nielsen, A.,
Casnovsky, J., & van den Berg, A. (2022). Examining geographic food
access, food insecurity, and urbanicity among diverse, low-income
participants in Austin, Texas. *International Journal of Environmental
Research and Public Health, 19(9)*.
<https://doi.org/10.3390/ijerph19095108>  
  
Lopez-Class, M., & Hosler, A. S. (2010). Assessment of community food
resources: A Latino neighborhood study in upstate New York. *Journal of
Poverty, 14(4)*, 369–381.
<https://doi.org/10.1080/10875549.2010.517070>  
  
Myers, A. M., & Painter, M. A. (2017). Food insecurity in the United
States of America: An examination of race/ethnicity and nativity. *Food
Security, 9(6)*, 1419–1432.
<https://doi.org/10.1007/s12571-017-0733-8>  
  
Nam, Y., Huang, J., Heflin, C., & Sherraden, M. (2015). Racial and
ethnic disparities in food insufficiency: Evidence from a statewide
probability sample. *Journal of the Society for Social Work and
Research, 6(2)*, 201–228.
<https://www.journals.uchicago.edu/doi/10.1086/681574>  
  
Odoms-Young, A. M. (2018). Examining the impact of structural racism on
food insecurity: Implications for addressing racial/ethnic disparities.
*Family & Community Health, 41*(Suppl 2 FOOD INSECURITY AND OBESITY),
S3–S6. <https://doi.org/10.1097/FCH.0000000000000183>  
  
Ramphul, R. (2020). *Using Spatial Methods To Better Understand Food
Insecurity And Snap Under-Participation In Texas* \[Master’s thesis,
UTHealth School of Public Health\]. Dissertations & Theses (Open
Access).
<https://digitalcommons.library.tmc.edu/uthsph_dissertsopen/227>  
  
Samuel, L. J., Crews, D. C., Swenor, B. K., et al. (2023). Supplemental
Nutrition Assistance Program access and racial disparities in food
insecurity. *JAMA Network Open, 6(6)*, e2320196.
<https://doi.org/10.1001/jamanetworkopen.2023.20196>  
  
USDA (2025). Food Security in the U.S. - Key Statistics & Graphics.
Available at:
<https://www.ers.usda.gov/topics/food-nutrition-assistance/food-security-in-the-us/key-statistics-graphics#>:~:text=13.5%20percent%20(18.0%20million)%20of,(17.0%20million)%20in%202022.  
  
Walker, R. E., Keane, C. R., & Burke, J. G. (2010). Disparities and
access to healthy food in the United States: A review of food deserts
literature. *Health & Place, 16(5)*, 876–884.
<https://doi.org/10.1016/j.healthplace.2010.04.013>

</div>
