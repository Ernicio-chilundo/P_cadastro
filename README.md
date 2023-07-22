# P_cadastro

#Quantas pessoas cadastradas M/F e a idade média

# Quantas pessoas cadastradas

# A média de idade.

# Uma lista com mulheres.

# Uma lista com pessoas de idade acima da média.

galera = []
pessoa = {}
soma = média = 0
while True:
 pessoa.clear()
 pessoa["Nome"] = str (input("Nome: "))
 while True:
  pessoa["Sexo"] = str (input("Sexo[M/F]: ")).upper()[0]
  if pessoa["Sexo"] in "MF":
   break
  print("Erro! por favor digite apenas M/F.")
 pessoa["Idade"] = int (input("Idade: "))
 soma += pessoa["Idade"]
 galera.append(pessoa.copy())
 while True:
  resp = str(input("Quero continuar?[S/N]: ")).upper()[0]
  if resp in "SN":
   break
  print("Erro! Responda apenas com sim ou não ")
 if resp == "N":
  break
print("~~"*29)
if len(galera) <= 1:
 print(f"\033[1;32mA>>\033[m Ao todo temos {len(galera)} pessoa cadastrada.")
elif len(galera) > 1:
 print(f"\033[1;32mA>>\033[m Ao todo temos {len(galera)} pessoas cadastradas.")
média = soma / len(galera)
print(f"\033[1;32mB>>\033[m A média de idade é de {média} anos.")
print("\033[1;32mC>>\033[m As mulheres cadastradas foram :")
for p in galera:
 if p["Sexo"] == "F":
  print(f"\033[1;35m>\033[m {p['Nome']}.")
print("\033[1;32mD>>\033[m Lista de pessoas com idade acima da média:")
for p in galera:
 if p["Idade"] >= média:
  for k, v in p.items():
   print(f"\033[1;35m>\033[m {k} = {v}.")
print()
