import mysql.connector

conexao = mysql.connector.connect (
    host='localhost',
    user='root',
    password='20163540',
    database='estudos',
)

cursor = conexao.cursor()

#CRUD


comando = f'SELECT * FROM VENDAS'
cursor.execute(comando)
# conexao.commit() #Edita o banco de dados
resultado = cursor.fetchall()_ # lê o banco de dados
print (resultado)


cursor.close()
conexao.close()
