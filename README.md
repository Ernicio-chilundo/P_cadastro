# P_cadastro
Quantas pessoas cadastradas M/F e a idade média
# Quantas pessoas cadastradas

# A média de idade.

# Uma lista com mulheres.

# Uma lista com idade acima da média.

pessoa = {}
while True:
 pessoa.clear()
 pessoa["Nome"] = str (input("Nome: "))
 while True:
  pessoa["Sexo"] = str (input("Sexo[M/F]: ")).upper()[0]
  if pessoa["Sexo"] in "MF":
   break
  print("Erro! por favor digite apenas M/F.")
 pessoa["Idade"] = int (input("Idade: "))


