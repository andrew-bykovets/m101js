
**Question**

Download Handouts: [grades.zip](https://github.com/fabiodelabruna/m101js/raw/master/homework-6.2/grades.zip)

Who is the easiest grader on campus?

Download the handout and import the grades collection using the following command.

```
mongoimport --drop -d test -c grades grades.json
```

Documents in the grades collection look like this.

```
{
    "_id" : ObjectId("50b59cd75bed76f46522c392"),
    "student_id" : 10,
    "class_id" : 5,
    "scores" : [
        {
            "type" : "exam",
            "score" : 69.17634380939022
        },
        {
            "type" : "quiz",
            "score" : 61.20182926719762
        },
        {
            "type" : "homework",
            "score" : 73.3293624199466
        },
        {
            "type" : "homework",
            "score" : 15.206314042622903
        },
        {
            "type" : "homework",
            "score" : 36.75297723087603
        },
        {
            "type" : "homework",
            "score" : 64.42913107330241
        }
    ]
}
```

There are documents for each student (student_id) across a variety of classes (class_id). Note that not all students in the same class have the same exact number of assessments. Some students have three homework assignments, etc.

Your task is to calculate the class with the best average student performance. This involves calculating an average for each student in each class of all non-quiz assessments and then averaging those numbers to get a class average. To be clear, each student's average should include only exams and homework grades.  **Don't include their quiz scores in the calculation.**

What is the class_id which has the highest average student performance? Choose the correct class_id below.

**Answer**

```
1
```