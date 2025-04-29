import time
import threading

def cronometro():
    print("Cronômetro iniciado! Pressione 'Ctrl + C' para parar.")
    segundos = 0
    try:
        while True:
            time.sleep(1)
            segundos += 1
            print(f"Tempo: {segundos} segundos", end="\r")
    
    except KeyboardInterrupt:  # Caso o usuário pressione 'Ctrl + C'
        print(f"\nCronômetro parado em {segundos} segundos.")
        return  # Retorna ao menu principal

def temporizador(segundos):
    print(f"Temporizador iniciado: {segundos} segundos")
    while segundos:
        time.sleep(1)
        segundos -= 1
        print(f"Tempo restante: {segundos} segundos", end="\r")
    print("\033[1;35m\nTempo esgotado!\033[0m")

def configuracoes_temporizador():
    print("\nConfiguração do Temporizador:")
    minutos = int(input("Quantos minutos? "))
    segundos = minutos * 60
    return segundos

if __name__ == "__main__":
    while True:
        try:
            print('\n=-=--=-=-=-=-=-=-=-=-=-=-=') 
            print("Escolha uma opção:")
            print("1 - Cronômetro")
            print("2 - Temporizador")
            print("3 - Configurar Temporizador")
            print("4 - Sair")
            print('=-=--=-=-=-=-=-=-=-=-=-=-=\n')
            opcao = input("Digite sua escolha: ")

            if opcao == "1":
                cronometro()  # Retorna ao menu após o cronômetro ser interrompido
            elif opcao == "2":
                segundos = int(input("Digite o tempo em segundos: "))
                temporizador(segundos)
            elif opcao == "3":
                segundos = configuracoes_temporizador()
                temporizador(segundos)
            elif opcao == "4":
                print("\033[1;31mSaindo...\033[0m")
                break
            else:
                print("Opção inválida. Tente novamente.")
        
        except KeyboardInterrupt:  # Captura o KeyboardInterrupt para impedir que o programa termine
            print("\nOperação interrompida. Retornando ao menu...\n")
            continue  # Retorna ao menu principal sem sair do programa
