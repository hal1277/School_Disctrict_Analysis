# School Disctrict Analysis

## Overview - School District Analysis

The purpose of this analysis is to help Maria and the school board analyze recent math and reading grades at the 15 schools in the district.  After analyzing the initial results it appeared to the board that there is possible academic dishonesty at Thomas High School specifically relating to the grades reported from the 9th grade students.  Therefore Maria asked for help to remove the 9th grade results from the intial analysis and re-calculate the school and district summaries.  

## Results

In order to complete the analysis without the scores from the 9th grade at Thomas High School the scores first had to be replaced with NaN to exclude them from any calculations.  

|       |   Student ID | student_name    | gender   | grade   | school_name        |   reading_score |   math_score |
|------:|-------------:|:----------------|:---------|:--------|:-------------------|----------------:|-------------:|
| 39165 |        39165 | Donna Howard    | F        | 12th    | Thomas High School |              99 |           90 |
| 39166 |        39166 | Dawn Bell       | F        | 10th    | Thomas High School |              95 |           70 |
| 39167 |        39167 | Rebecca Tanner  | F        | 9th     | Thomas High School |             nan |          nan |
| 39168 |        39168 | Desiree Kidd    | F        | 10th    | Thomas High School |              99 |           90 |
| 39169 |        39169 | Carolyn Jackson | F        | 11th    | Thomas High School |              95 |           75 |

And, to calculate the percentages at Thomas High School the count of students in the 9th grade had to be removed.  The updated percentages were then used to replace the previously calculated values in the summary dataframes.  The top chart below reflects the first analysis and the second chart shows the changes afer removing the Thomas High School 9th grade scores. 

|    |   Total Schools | Total Students   | Total Budget   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|---:|----------------:|:-----------------|:---------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
|  0 |              15 | 39,170           | $24,649,428.00 |                   79 |                    81.9 |               75 |                  86 |                  65 |



|    |   Total Schools | Total Students   | Total Budget   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|---:|----------------:|:-----------------|:---------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
|  0 |              15 | 39,170           | $24,649,428.00 |                 78.9 |                    81.9 |             74.8 |                85.7 |                64.9 |

There are only 461 students in the 9th grade at Thomas High School out of the 39,170 total students in the district so removing the 9th grade scores has no effect on the overall district summary since the removed students acount for only 1% of the total students.  

In the initial analysis the average math and reading scores per grade at Thomas High School can be seen in the table below.  There was very litle variation between the scores of the different grades. 

Math Scores:

|                       |   9th |   10th |   11th |   12th |
|:----------------------|------:|-------:|-------:|-------:|
| Bailey High School    |  77.1 |   77   |   77.5 |   76.5 |
| Cabrera High School   |  83.1 |   83.2 |   82.8 |   83.3 |
| Figueroa High School  |  76.4 |   76.5 |   76.9 |   77.2 |
| Ford High School      |  77.4 |   77.7 |   76.9 |   76.2 |
| Griffin High School   |  82   |   84.2 |   83.8 |   83.4 |
| Hernandez High School |  77.4 |   77.3 |   77.1 |   77.2 |
| Holden High School    |  83.8 |   83.4 |   85   |   82.9 |
| Huang High School     |  77   |   75.9 |   76.4 |   77.2 |
| Johnson High School   |  77.2 |   76.7 |   77.5 |   76.9 |
| Pena High School      |  83.6 |   83.4 |   84.3 |   84.1 |
| Rodriguez High School |  76.9 |   76.6 |   76.4 |   77.7 |
| Shelton High School   |  83.4 |   82.9 |   83.4 |   83.8 |
| Thomas High School    |  83.6 |   83.1 |   83.5 |   83.5 |
| Wilson High School    |  83.1 |   83.7 |   83.2 |   83   |
| Wright High School    |  83.3 |   84   |   83.8 |   83.6 |

Reading Scores:

|                       |   9th |   10th |   11th |   12th |
|:----------------------|------:|-------:|-------:|-------:|
| Bailey High School    |  81.3 |   80.9 |   80.9 |   80.9 |
| Cabrera High School   |  83.7 |   84.3 |   83.8 |   84.3 |
| Figueroa High School  |  81.2 |   81.4 |   80.6 |   81.4 |
| Ford High School      |  80.6 |   81.3 |   80.4 |   80.7 |
| Griffin High School   |  83.4 |   83.7 |   84.3 |   84   |
| Hernandez High School |  80.9 |   80.7 |   81.4 |   80.9 |
| Holden High School    |  83.7 |   83.3 |   83.8 |   84.7 |
| Huang High School     |  81.3 |   81.5 |   81.4 |   80.3 |
| Johnson High School   |  81.3 |   80.8 |   80.6 |   81.2 |
| Pena High School      |  83.8 |   83.6 |   84.3 |   84.6 |
| Rodriguez High School |  81   |   80.6 |   80.9 |   80.4 |
| Shelton High School   |  84.1 |   83.4 |   84.4 |   82.8 |
| Thomas High School    |  83.7 |   84.3 |   83.6 |   83.8 |
| Wilson High School    |  83.9 |   84   |   83.8 |   84.3 |
| Wright High School    |  83.8 |   83.8 |   84.2 |   84.1 |

The school summary from the intital analysis is:

|                       | School Type   |   Total Students | Total School Budget   | Per Student Budget   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing | Spending Ranges (Per Student)   | School Size        |
|:----------------------|:--------------|-----------------:|:----------------------|:---------------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|:--------------------------------|:-------------------|
| Bailey High School    | District      |             4976 | $3,124,928.00         | $628.00              |              77.0484 |                 81.034  |          66.6801 |             81.9333 |             54.6423 | $585-629                        | Large (2000-5000)  |
| Cabrera High School   | Charter       |             1858 | $1,081,356.00         | $582.00              |              83.0619 |                 83.9758 |          94.1335 |             97.0398 |             91.3348 | <$584                           | Medium (1000-2000) |
| Figueroa High School  | District      |             2949 | $1,884,411.00         | $639.00              |              76.7118 |                 81.158  |          65.9885 |             80.7392 |             53.2045 | $630-644                        | Large (2000-5000)  |
| Ford High School      | District      |             2739 | $1,763,916.00         | $644.00              |              77.1026 |                 80.7463 |          68.3096 |             79.299  |             54.2899 | $630-644                        | Large (2000-5000)  |
| Griffin High School   | Charter       |             1468 | $917,500.00           | $625.00              |              83.3515 |                 83.8168 |          93.3924 |             97.139  |             90.5995 | $585-629                        | Medium (1000-2000) |
| Hernandez High School | District      |             4635 | $3,022,020.00         | $652.00              |              77.2898 |                 80.9344 |          66.753  |             80.863  |             53.5275 | $645-675                        | Large (2000-5000)  |
| Holden High School    | Charter       |              427 | $248,087.00           | $581.00              |              83.8033 |                 83.815  |          92.5059 |             96.2529 |             89.2272 | <$584                           | Small (<1000)      |
| Huang High School     | District      |             2917 | $1,910,635.00         | $655.00              |              76.6294 |                 81.1827 |          65.6839 |             81.3164 |             53.5139 | $645-675                        | Large (2000-5000)  |
| Johnson High School   | District      |             4761 | $3,094,650.00         | $650.00              |              77.0725 |                 80.9664 |          66.0576 |             81.2224 |             53.5392 | $645-675                        | Large (2000-5000)  |
| Pena High School      | Charter       |              962 | $585,858.00           | $609.00              |              83.8399 |                 84.0447 |          94.5946 |             95.9459 |             90.5405 | $585-629                        | Small (<1000)      |
| Rodriguez High School | District      |             3999 | $2,547,363.00         | $637.00              |              76.8427 |                 80.7447 |          66.3666 |             80.2201 |             52.9882 | $630-644                        | Large (2000-5000)  |
| Shelton High School   | Charter       |             1761 | $1,056,600.00         | $600.00              |              83.3595 |                 83.7257 |          93.8671 |             95.8546 |             89.8921 | $585-629                        | Medium (1000-2000) |
| Thomas High School    | Charter       |             1635 | $1,043,130.00         | $638.00              |              83.4183 |                 83.8489 |          93.2722 |             97.3089 |             90.948  | $630-644                        | Medium (1000-2000) |
| Wilson High School    | Charter       |             2283 | $1,319,574.00         | $578.00              |              83.2742 |                 83.9895 |          93.8677 |             96.5396 |             90.5826 | <$584                           | Large (2000-5000)  |
| Wright High School    | Charter       |             1800 | $1,049,400.00         | $583.00              |              83.6822 |                 83.955  |          93.3333 |             96.6111 |             90.3333 | <$584                           | Medium (1000-2000) |

And after removing the scores for the 9th grade at Thomas High School the summary is:

|                       | School Type   |   Total Students | Total School Budget   | Per Student Budget   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing | Spending Ranges (Per Student)   | School Size        |
|:----------------------|:--------------|-----------------:|:----------------------|:---------------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|:--------------------------------|:-------------------|
| Bailey High School    | District      |             4976 | $3,124,928.00         | $628.00              |              77.0484 |                 81.034  |          66.6801 |             81.9333 |             54.6423 | $585-629                        | Large (2000-5000)  |
| Cabrera High School   | Charter       |             1858 | $1,081,356.00         | $582.00              |              83.0619 |                 83.9758 |          94.1335 |             97.0398 |             91.3348 | <$584                           | Medium (1000-2000) |
| Figueroa High School  | District      |             2949 | $1,884,411.00         | $639.00              |              76.7118 |                 81.158  |          65.9885 |             80.7392 |             53.2045 | $630-644                        | Large (2000-5000)  |
| Ford High School      | District      |             2739 | $1,763,916.00         | $644.00              |              77.1026 |                 80.7463 |          68.3096 |             79.299  |             54.2899 | $630-644                        | Large (2000-5000)  |
| Griffin High School   | Charter       |             1468 | $917,500.00           | $625.00              |              83.3515 |                 83.8168 |          93.3924 |             97.139  |             90.5995 | $585-629                        | Medium (1000-2000) |
| Hernandez High School | District      |             4635 | $3,022,020.00         | $652.00              |              77.2898 |                 80.9344 |          66.753  |             80.863  |             53.5275 | $645-675                        | Large (2000-5000)  |
| Holden High School    | Charter       |              427 | $248,087.00           | $581.00              |              83.8033 |                 83.815  |          92.5059 |             96.2529 |             89.2272 | <$584                           | Small (<1000)      |
| Huang High School     | District      |             2917 | $1,910,635.00         | $655.00              |              76.6294 |                 81.1827 |          65.6839 |             81.3164 |             53.5139 | $645-675                        | Large (2000-5000)  |
| Johnson High School   | District      |             4761 | $3,094,650.00         | $650.00              |              77.0725 |                 80.9664 |          66.0576 |             81.2224 |             53.5392 | $645-675                        | Large (2000-5000)  |
| Pena High School      | Charter       |              962 | $585,858.00           | $609.00              |              83.8399 |                 84.0447 |          94.5946 |             95.9459 |             90.5405 | $585-629                        | Small (<1000)      |
| Rodriguez High School | District      |             3999 | $2,547,363.00         | $637.00              |              76.8427 |                 80.7447 |          66.3666 |             80.2201 |             52.9882 | $630-644                        | Large (2000-5000)  |
| Shelton High School   | Charter       |             1761 | $1,056,600.00         | $600.00              |              83.3595 |                 83.7257 |          93.8671 |             95.8546 |             89.8921 | $585-629                        | Medium (1000-2000) |
| Thomas High School    | Charter       |             1635 | $1,043,130.00         | $638.00              |              83.3509 |                 83.8961 |          93.1857 |             97.0187 |             90.6303 | $630-644                        | Medium (1000-2000) |
| Wilson High School    | Charter       |             2283 | $1,319,574.00         | $578.00              |              83.2742 |                 83.9895 |          93.8677 |             96.5396 |             90.5826 | <$584                           | Large (2000-5000)  |
| Wright High School    | Charter       |             1800 | $1,049,400.00         | $583.00              |              83.6822 |                 83.955  |          93.3333 |             96.6111 |             90.3333 | <$584                           | Medium (1000-2000) |

For Thomas High School after removing the 9th grade scores the average math score dropped, the average reading score increased, the % passing math decreased, the % passing reading decreased, and the overaall passing % decreased.  

The analysis of scores by school size shows no change between the two analyses. 

Including Thomas High School 9th grade scores:

| School Size        |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|:-------------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
| Small (<1000)      |                 83.8 |                    83.9 |               94 |                  96 |                  90 |
| Medium (1000-2000) |                 83.4 |                    83.9 |               94 |                  97 |                  91 |
| Large (2000-5000)  |                 77.7 |                    81.3 |               70 |                  83 |                  58 |

Excluding Thomas High School 9th grade scores:

| School Size        |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|:-------------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
| Small (<1000)      |                 83.8 |                    83.9 |               94 |                  96 |                  90 |
| Medium (1000-2000) |                 83.4 |                    83.9 |               94 |                  97 |                  91 |
| Large (2000-5000)  |                 77.7 |                    81.3 |               70 |                  83 |                  58 |

The analysis of scores by school spending shows no change in the results whether including Thomas High School 9th grade scores or not.  

Including Thomas High School 9th grade scores:

| Spending Ranges (Per Student)   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|:--------------------------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
| <$584                           |                 83.5 |                    83.9 |               93 |                  97 |                  90 |
| $585-629                        |                 81.9 |                    83.2 |               87 |                  93 |                  81 |
| $630-644                        |                 78.5 |                    81.6 |               73 |                  84 |                  63 |
| $645-675                        |                 77   |                    81   |               66 |                  81 |                  54 |


Excluding Thomas High School 9th grade scores:

| Spending Ranges (Per Student)   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|:--------------------------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
| <$584                           |                 83.5 |                    83.9 |               93 |                  97 |                  90 |
| $585-629                        |                 81.9 |                    83.2 |               87 |                  93 |                  81 |
| $630-644                        |                 78.5 |                    81.6 |               73 |                  84 |                  63 |
| $645-675                        |                 77   |                    81   |               66 |                  81 |                  54 |

And, finally the analysis of scores by school type 

Including Thomas High School 9th grade score:

| School Type   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|:--------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
| Charter       |                 83.5 |                    83.9 |               94 |                  97 |                  90 |
| District      |                 77   |                    81   |               67 |                  81 |                  54 |

Excluding Thomas High School 9th grade score:

| School Type   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|:--------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
| Charter       |                 83.5 |                    83.9 |               94 |                  97 |                  90 |
| District      |                 77   |                    81   |               67 |                  81 |                  54 |

The school rankings also remain unchanged from the analysis including Thomas High School 9th grade scores vs. not including Thomas High School 9th grade scores. 

Top 5 schools with Thomas High School 9th grade included:

|                     | School Type   |   Total Students | Total School Budget   | Per Student Budget   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing |
|:--------------------|:--------------|-----------------:|:----------------------|:---------------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|
| Cabrera High School | Charter       |             1858 | $1,081,356.00         | $582.00              |              83.0619 |                 83.9758 |          94.1335 |             97.0398 |             91.3348 |
| Thomas High School  | Charter       |             1635 | $1,043,130.00         | $638.00              |              83.4183 |                 83.8489 |          93.2722 |             97.3089 |             90.948  |
| Griffin High School | Charter       |             1468 | $917,500.00           | $625.00              |              83.3515 |                 83.8168 |          93.3924 |             97.139  |             90.5995 |
| Wilson High School  | Charter       |             2283 | $1,319,574.00         | $578.00              |              83.2742 |                 83.9895 |          93.8677 |             96.5396 |             90.5826 |
| Pena High School    | Charter       |              962 | $585,858.00           | $609.00              |              83.8399 |                 84.0447 |          94.5946 |             95.9459 |             90.5405 |

Top 5 schools with Thomas High School 9th grade excluded:

|                     | School Type   |   Total Students | Total School Budget   | Per Student Budget   |   Average Math Score |   Average Reading Score |   % Passing Math |   % Passing Reading |   % Overall Passing | Spending Ranges (Per Student)   | School Size        |
|:--------------------|:--------------|-----------------:|:----------------------|:---------------------|---------------------:|------------------------:|-----------------:|--------------------:|--------------------:|:--------------------------------|:-------------------|
| Cabrera High School | Charter       |             1858 | $1,081,356.00         | $582.00              |              83.0619 |                 83.9758 |          94.1335 |             97.0398 |             91.3348 | <$584                           | Medium (1000-2000) |
| Thomas High School  | Charter       |             1635 | $1,043,130.00         | $638.00              |              83.3509 |                 83.8961 |          93.1857 |             97.0187 |             90.6303 | $630-644                        | Medium (1000-2000) |
| Griffin High School | Charter       |             1468 | $917,500.00           | $625.00              |              83.3515 |                 83.8168 |          93.3924 |             97.139  |             90.5995 | $585-629                        | Medium (1000-2000) |
| Wilson High School  | Charter       |             2283 | $1,319,574.00         | $578.00              |              83.2742 |                 83.9895 |          93.8677 |             96.5396 |             90.5826 | <$584                           | Large (2000-5000)  |
| Pena High School    | Charter       |              962 | $585,858.00           | $609.00              |              83.8399 |                 84.0447 |          94.5946 |             95.9459 |             90.5405 | $585-629                        | Small (<1000)      |

## Summary

After re-doing the original analysis but with the 9th grade scores from Thomas High School excluded we can see that at Thomas High School the average math score dropped, the average reading score increased, the % passing math decreased, the % passing reading decreased, and the overaall passing % decreased at Thomas High School.  However, the changes were very small and since the 9th grade students at Thomas High School only make up 1.18% of the total students in the district their exclusion from the data set has no statisitcally significant impact of the overal district results.  As well when looking at the 9th grade scores at Thomas High School they are not statistically significantly different from the other grades.  Thomas High School is ranked 2nd in the district so potentially there could be an issue with all the grades but their results are in line with what is expected from a charter school with a similar per capita spend.  Based on the above analysis there does not seem to be evidence of academic dishonesty within the 9th grade scores at Thomas High School.  