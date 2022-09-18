//1.Create a movie TABLE
CREATE TABLE Movie(
    movie_id int NOT NULL,
    movie_title varchar(20),
    movie_year int,
    movie_length int,
    movie_lang varchar(20),
    Artist_name varchar(20),
    Director_name varchar(20),
    Video_url varchar,
   PRIMARY KEY (movie_id)
)

INSERT INTO Movie(movie_id,movie_title,movie_year,movie_length,movie_lang,Artist_name,Director_name,Video_url)
VALUES(100,Vaali,1998,183,Tamil,Ajith Kumar,SJ Surya,https://www.youtube.com/watch?v=ATiRY0cRlak),
(101,Enthiran,2010,140,Tamil,Rajinikanth,Shankar,https://www.youtube.com/watch?v=sGdoQEeIkxI),
(102,Azhagiya tamizhmagan,2007,193,Tamil,Vijay,Bharathan,https://www.youtube.com/watch?v=Kg34OISUzlM),
(103,24,2016,134,Tamil,Suriya,Vikram kumar,https://www.youtube.com/watch?v=wqXE_es_I3M),
(104,Alavandhan,2001,162,Tamil,Kamal Haasan,Suresh Krissna,https://www.youtube.com/watch?v=Z_4ly77mjEM),
(105,Irumugan,2016,138,Tamil,Vikram,Anand Shankar,https://www.youtube.com/watch?v=0sjudcc3ItU)

//2.Create a movie with multiple genres
Create Table Genres(
    movie_id int NOT NULL,
    gen_id int,
    gen_title varchar(20)
);

INSERT INTO Genres(movie_id,gen_id,gen_title)
VALUES(100,1001,Drama),
(101,1002,Science fiction),
(102,1003,Drama),
(103,1004,Science fiction),
(104,1005,Psychological Thriller),
(105,1006,Action Thriller)

//3.Movie can have multiple reviews and Review can belongs to a user
Create Table Rating(
    movie_id int NOT NULL,
    review_id int,
    review_stars float,
    user_rating
);

INSERT INTO Rating(movie_id,review_id,review_stars,user_rating)
VALUES(100,9001,8.40,263575),
(101,9002,7.90,20207),
(102,9003,8.30,202778),
(103,9004,8.60,779489),
(104,9005,8,92,956756),
(105,9006,8.98,745634)

//4.Artist can have multiple skills
Create Table Artist(
    Artist_name varchar(20),
    art_id int NOT NULL,
    Art_gender char,
    Art_skills varchar(20)
);

INSERT INTO Artist(Artist_name,art_id,Art_gender,Art_skills)
VALUES(Ajith Kumar,50,Male,Acting),
(Ajith Kumar,50,Male,Racer),
(Vijay,51,Male,Singing),
(Vijay,51,Male,Dancer),
(Vijay,51,Male,Acting),
(Suriya,52,Male,Acting),
(Suriya,52,Male,Singing),
(Kamal Haasan,53,Male,Acting),
(Kamal Haasan,53,Male,Singing),
(Kamal Haasan,53,Male,Writing),
(Vikram,54,Male,Acting),
(Vikram,54,Male,Singing)

//5.Artist can perform multiple role in a single film
Create Table Role(
    movie_id int NOT NULL,
    movie_title varchar(20),
    art_id int NOT NULL,
    Artist_name varchar(20),
    Art_role varchar(20)
);

INSERT INTO Role(movie_id,movie_title,art_id,Art_role)
VALUES(100,Vaali,50,Ajith Kumar,Shiva,Hero),
(100,Vaali,50,Ajith Kumar,Deva,Villain),
(101,Enthiran,51,Rajinikanth,Vaseegaran,Scientist),
(101,Enthiran,51,Rajinikanth,Chitti,Evil Robot),
(102,Azhagiya Tamizhmagan,52,Vijay,Guru,Hero),
(102,Azhagiya Tamizhmagan,52,Vijay,Prasad,Villain),
(103,24,53,Suriya,Sethuram,Scientist),
(103,24,53,Suriya,Athreya,Villain),
(103,24,53,Suriya,Mani,Hero Watch Mechanic),
(104,Alavandhan,54,Kamal Haasan,Major Vijay Kumar,Hero),
(104,Alavandhan,54,Kamal Haasan,Nandha Kumar,Villain),
(105,Irumugan,55,Vikram,Akilan Vinod,Hero),
(105,Irumugan,55,Vikram,Dr Love,Villain)




