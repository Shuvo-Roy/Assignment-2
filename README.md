1.	What is PostgreSQL?
Answer:  PostgreSQL একটি ওপেন-সোর্স রিলেশনাল ডেটাবেজ (Relational Database RDMS), যা SQL এর সাহায্যে  তথ্য সংরক্ষন করা ও বিশ্লেষণ করে । এই ডেটাবেজ ওপেনসোর্স ও এর এক্সটেন্সিবিলিটি অনেক যেখানে আমারা আমাদের প্রয়োজন অনুযায়ী নতুন নতুন Functionality  যুক্ত করতে পারি।

2.	What is the purpose of a database schema in PostgreSQL?
Answer: Schema হলো ডেটাবেজের মাধ্যমে একটি লজিক তৈরি করা যা টেবিল,ভিউ ও ফাংশন কে রাখে। আমরা একটি স্কিমা এর মধ্যে অনেক গুল স্কিমা রাখতে পারি যা বড় কোন প্রোজেক্ট এর ডেটা সুন্দর ভাবে সাজানো যায়। স্কিমা যেভাবে বানাতে পারি
CREATE SCHEMA myschema;

3.	What is the purpose of a database schema in PostgreSQL?
Answer: 
Primary Key: একটি টেবিলের প্রতিটি রেকর্ডকে ইউনিকভাবে শনাক্ত করার জন্য ব্যবহৃত হয়। এটি কখনো NULL বা ডুপ্লিকেট হতে পারে না।
Foreign Key: একটি টেবিলে অন্য টেবিলের Primary Key-এর রেফারেন্স হিসাবে ব্যবহৃত হয়। এটি টেবিলগুলোর মধ্যে সম্পর্ক (relationship) তৈরি করে এবং রেফারেন্স ইন্টিগ্রিটি বজায় রাখে।

4.	What is the significance of the JOIN operation, and how does it work in PostgreSQL?
Answer:  JOIN অপারেশন ব্যবহার করে আমরা একাধিক টেবিলের ডেটা একসাথে মিলিয়ে দেখতে পারি, যেখানে দুটি টেবিলের একে অপরের সাথে সংযুক্ত থাকে Primary এবং Foreign Key দিয়ে।
কয়েক ধরনের JOIN আছে PostgreSQL এর মধ্যে। যেমন –
•	INNER JOIN
•	LEFT JOIN
•	RIGHT JOIN
•	FULL JOIN 
উদাহরণ
SELECT r.name, s.location
FROM rangers r
JOIN sightings s ON r.ranger_id = s.ranger_id;

5.	Explain the GROUP BY clause and its role in aggregation operations.
Answer: GROUP BY হলো টেবিলের এক বা একাধিক কলামে একই মান বা তথ্য একটি আলাদা টেবিলে দেখা
যেমনঃ যোগ,বিয়োগ,গুন,ভাগ ইত্যাদি।
SELECT CustomerID, SUM(OrderAmount) AS TotalOrderAmount
FROM Orders
GROUP BY CustomerID;
