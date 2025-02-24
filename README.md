user = SELECT * FROM users WHERE Username = '' OR 1=1 --;
print(user)

SELECT * FROM users WHERE Username = '' AND (SELECT 1 FROM users WHERE id=1) = 1 --
