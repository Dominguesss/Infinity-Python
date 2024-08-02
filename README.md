# Dicionário para armazenar os alunos
alunos = {}

def AdicionarAluno():
    matricula = input("Digite o número de matrícula do aluno: ")
    nome = input("Digite o nome do aluno: ")
    alunos[matricula] = nome
    print(f"Aluno {nome} adicionado com sucesso!")

def RemoverAluno():
    matricula = input("Digite o número de matrícula do aluno a ser removido: ")
    if matricula in alunos:
        del alunos[matricula]
        print(f"Aluno com matrícula {matricula} removido com sucesso!")
    else:
        print("Matrícula não encontrada.")

def AtualizarAluno():
    matricula = input("Digite o número de matrícula do aluno a ser atualizado: ")
    if matricula in alunos:
        nome = input("Digite o novo nome do aluno: ")
        alunos[matricula] = nome
        print(f"Aluno com matrícula {matricula} atualizado com sucesso!")
    else:
        print("Matrícula não encontrada.")

def VerAlunos():
    if alunos:
        print("Lista de alunos cadastrados:")
        for matricula, nome in alunos.items():
            print(f"Matrícula: {matricula}, Nome: {nome}")
    else:
        print("Nenhum aluno cadastrado.")

# Menu de opções
def menu():
    while True:
        print("\nMenu:")
        print("1. Adicionar Aluno")
        print("2. Remover Aluno")
        print("3. Atualizar Aluno")
        print("4. Ver Alunos")
        print("5. Sair")
        
        opcao = input("Escolha uma opção: ")
        
        if opcao == '1':
            AdicionarAluno()
        elif opcao == '2':
            RemoverAluno()
        elif opcao == '3':
            AtualizarAluno()
        elif opcao == '4':
            VerAlunos()
        elif opcao == '5':
            print("Saindo do programa...")
            break
        else:
            print("Opção inválida. Tente novamente.")

# Executar o menu
menu()
