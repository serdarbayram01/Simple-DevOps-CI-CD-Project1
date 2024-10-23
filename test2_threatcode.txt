import sqlite3

def get_user(user_id):
    conn = sqlite3.connect('users.db')
    c = conn.cursor()
    c.execute("SELECT * FROM users WHERE id = " + user_id)
    user = c.fetchone()
    conn.close()
    return user

user_input = input("Kullanıcı ID'sini girin: ")
user = get_user(user_input)
