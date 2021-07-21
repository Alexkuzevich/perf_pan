Первое задание по SQL:

SELECT users.id AS id, CONCAT(users.first_name,' ',users.last_name) AS name, books.author AS author, GROUP_CONCAT(books.name SEPARATOR ',') AS books
FROM users
LEFT JOIN user_books ON age between 7 AND 17 AND users.id = user_books.user_id
LEFT JOIN books ON user_books.book_id = books.id
GROUP BY users.id
HAVING COUNT(DISTINCT(books.author)) = 1 AND COUNT(user_books.book_id) = 2
