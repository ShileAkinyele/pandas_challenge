# pandas_challenge

This piece of work consists of analysis on the data of schools and students consisting of math and reading test scores. In-depth analysis is done to magnify a trend in the performance of students across schools using various variables to establish a relationship. Variables used include the grade of students, school type, school size, and school spending. From this analysis we can see a relationship between school size and overall performance. This analysis is done in a bid to make informed decisions on school budgets and future priorities 


#Conclusion from  analysis 


Based on the data provided we can see that the size of the school and the budget of the school are directly proportional to the school type. Bigger sized schools are of a certain type and a certain type of school receives a higher budget. Districts are more populated and have a higher budget allocation than that of the schools that belong to the charter.
Based on the overall percentage pass rate, the top five schools belong to the Charter while the bottom five schools belong to the district. This denotes better grades amongst the schools in the charter than those in the district. A closer look at the average reading and math scores by grades (9-12) shows a fluctuation in average scores amongst grades. As such, it cannot be categorically said that there is a relationship between getting better reading /math scores and attaining a higher-class grade. Other factors which we have not accounted for in this analysis might be responsible for this.
Based on the analysis on School score by school size, it is seen that schools on the medium size perform better than schools on the large size. In general, this could be attributed to lesser pressure on resources available to students. Therefore, allowing students in medium sized schools to receive better quality of education.
Also, analysis based on school type shows that schools that belong to the Charter can record a higher overall pass rate (90.432244%) than that of the schools in the district (53.672208%). Also, the average reading and math scores of schools in the Charter are higher than those belonging to the district. This could also be related to the school size, being that Schools belonging to the districts are more on the larger side.
In conclusion, in terms of academic performance relating to math and reading, schools in the Charter type are doing better than those in the districts. To get a clearer view of the driving factors this analysis could have looked at other factors driving student’s performance/reading and math scores. Factors such as the bureaucracy involved in taking decisions that enhance growth in district schools should have been included. This could be represented by advanced learning facilities available.
Also, we could have looked at the relationship between the scores and the gender of the students to see if any relationship exists. Inclusion of more school rather than 15 schools as used in the data set would have better represented the school population.
Government will need to put a cap on the way students are accepted into district schools to maintain a capacity that will result in the quality of education being maximized by each student. Also, the budget could be targeted towards providing more services to fit the existing capacity. For example, the budget could be geared towards employing more capable teachers and increasing classrooms to reduce class size capacity and enable adequate attention been given to each student.

#SOURCE CODE
In [157]:school_types =school_data.set_index(["school_name"])["type"]  code code assisted with by TA

In [158]:per_school_counts = school_data_complete["school_name"].value_counts()  code assisted with by TA

In [161]:students_passing_math = school_data_complete[(school_data_complete["math_score"] >= 70)]
school_students_passing_math = students_passing_math.groupby(["school_name"]).count()["student_name"]  code assisted with by TA

In [162]: students_passing_reading = school_data_complete[(school_data_complete["reading_score"] >= 70)]
school_students_passing_reading = students_passing_reading.groupby(["school_name"]).count()["student_name"] code assisted with by TA

In [173]:     math_scores_by_grade=pd.DataFrame({'9th':ninth_grade_math_score,'10th':tenth_grade_math_score,"11th":eleventh_grade_math_score,'12th':twelfth_grade_math_score}) code assisted with by TA




