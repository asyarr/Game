import time
import random


print("""
   ============================================
   d8888b db    db d888b. 88 d8b   88   .o88b      
     88    db  db  88  88 88 88 b  88  dP       
     88      bd    8888P  88 88  b 88 8I  ooob    
     88      88    88     88 88   b88  db    8P 
     88      88    88     88 88    88   `d88P´ 

           d888b.   .d88b.   .d88b.  d888b
           88   I8 d8    8b  dP   Y8 88
           8888P´  88oooo88 8I       88oo
           88  8b  88    88  Yb   d8 88
           88   8b 88    88  `Y88P´  Y888P
   ============================================""")
time.sleep(2)



# O jogo poderá ser jogado em português ou inglês, por isso primeiro vamos perguntar em qual o idioma 
# o jogador quer jogar.

Lingua = True

idioma = 2

idioma = input("""    ==========================================

    Choose the language:

    1 - Portuguese _________________________

    2 - English ____________________________

    ==========================================

    Enter which option you want: """)

while not "1" <= idioma <= "2":
    idioma = input("""
    Invalid Input. Try again.

    ==========================================

    Choose the language:

    1 - Portuguese _________________________

    2 - English ____________________________

    ==========================================

    Enter which option you want: """)



# Após decidido o idioma iniciará um loop com as duas opções de idiomas.

while Lingua == True:

    # Jogo em português:

    if idioma == "1":
        print("""
    Carregando...""")
        time.sleep(1)
        
        # Coloquei as listas e as configurações do jogo para poder diferenciar entre português e inglês:

        qntJogador = 2
        nome = []
        tempos = []
        qntPergunta = 3
        jogador = 0
        index = 0

        
        print("""
    ============= BEM - VINDO  =============
        Esse  é  um  jogo  de velocidade de 
    digitação.   O jogo pode ser jogado por 
    2 ou até 4 jogadores, então pode chamar 
    os amigos e vamos começar a jogar.                    
    ========================================
            """)
        time.sleep(3)

        Menu = True
        
        # Aqui vai iniciar o loop do menu e ele ficará se repetindo até a pessoa pedir pra sair. 
        
        while Menu == True:
        
        
            opção = input("""
    ================= MENU =================

    1 - Jogar ______________________________

    2 - Configurações ______________________

    3 - Tutorial ___________________________

    4 - Créditos ___________________________

    5 - Sair _______________________________

    ========================================

    Digite qual a opção desejada: """)
     
            time.sleep(2)

            # Essa opção da início ao loop do jogo

            if opção == "1":
            
                jogo = True

                # o jogo foi colocado em loop caso o jogador queira jogar várias partidas.

                while jogo == True:
                    
                    # Além disso fizemos um jogo comm dois modos, o de matemática e o de digitação e le ta incluso 
                    # dentro do loop então se o jogador quiser escolher outro modo de jogo após uma partida ele consegue.

                    modo = input("""
    ====================================== 

    Escolha qual o modo de jogo:  

    1 - Matemática _________________________
    2 - Digitação __________________________  

    ======================================    

    Digite a opção desejada: """)

                    # Modo matemática:

                    if modo == "1":

                        for i in range(qntJogador):

                            # as perguntas e respostas foram botadas em listas e dentro do range pq aí elas 
                            # podem se repetira a cada jogador
                            pergunta = ["Quanto é 2+20? ", "Quanto é 4/2? ", "Quanto é 7-4? ", "Quanto é 8/2? ", "Quanto é 5x5? ", "Quanto é 9x9? ", "Quanto é raiz de 225? ", "Quanto é raiz de 64? ", "Quanto é 50+22? ", "Quanto é 15x3? ", "Quanto é 20x20? ", "Quanto é 40-2? "]

                            resposta = ["22", "2", "3", "4", "25", "81", "15", "8", "72", "45", "400", "38"]

                            jogador = jogador + 1 # aqui a gente exclui o jogador 0
                            print("")
                            nome.append(input("    Jogador " + str(jogador) + " seu nome: "))

                            print("""
    Vamos começar! Aperte ENTER quando estiver pronto
                            """)
                            input()
                            tempo_inicial = time.time() # aqui inicia a contagem da rodada!

                            for q in range(qntPergunta):
                                Pergunta_sorteada = random.choice(pergunta) # sorteia uma pergunta

                                resposta_digitada = input("    " + str(Pergunta_sorteada))

                                r_sorteada = pergunta.index(Pergunta_sorteada) # isso daqui serva para encontrarmos 
                                # a posição da pergunta, as perguntas e resposta estão na mesma posição na lista, 
                                # assim fica mais fácil fazer uma comparação
                                print("""
                                """)

                                while Pergunta_sorteada in pergunta:
                                    pergunta.remove(Pergunta_sorteada) # remove a pergunta da lista

                                    while not resposta_digitada == resposta[r_sorteada]:
                                        resposta_digitada = input("    " + str(Pergunta_sorteada)) 
                                        print("""
                                        """)
                                    
                                    if resposta_digitada == resposta[r_sorteada]:
                                        resposta.remove(resposta[r_sorteada])
                                        tempo_final = time.time() # quando a resposta for certa ele para o tempo
                                        continue

                            tempo_total = tempo_final - tempo_inicial # calcula o tempo da rodada

                            print('   ', nome[index], 'demorou', round(tempo_total, 1), 'segundos para responder as perguntas.')
                            index = index + 1            
                            tempos.append(float(tempo_total)) # adiocona o tempo numa lista
                            print("""
    Aguarde...
            """)
                            time.sleep(1)
                        podio = sorted(tempos)

                        if qntJogador == 2:

                            primeiro = tempos.index(podio[0])
                            segundo = tempos.index(podio[1])
                            
                            print("    Parabéns", nome[primeiro], "você foi o ganhou.")
                            print('')
                            print("    ", nome[segundo], "você foi o segundo.")
                            print('')

                        else:
                            primeiro = tempos.index(podio[0])
                            segundo = tempos.index(podio[1])
                            terceiro = tempos.index(podio[2])

                            print("    Parabéns", nome[primeiro], "você ganhou.")
                            print('')
                            print("    ", nome[segundo], "você foi o segundo.")
                            print('')
                            print("    ", nome[terceiro], "você foi o terceiro.")
                            print('')

                        # reinicia as variáveis pra não repetir os nomes na próxima rodada e dar tudo errado:

                        jogador = 0 
                        index = 0
                        nome = []
                        tempos = []

                        # aqui é caso a pessoa queira joga novamente

                        final = input("    Deseja jogar novamente(s/n): ")

                        if final == "s":
                            pass
                        elif final == "n": 
                            jogo = False # quebra o loop e volta pro menu
                        else:
                            while True:
                                print('')
                                print("    Entrada invalida")
                                print('')
                                final = input("    Deseja jogar novamente(s/n): ")
                                if final == "s":
                                    break
                                elif final == "n":
                                    jogo = False 
                                    break
                        time.sleep(3)

                    # Modo digitação

                    elif modo == "2":
                        for i in range(qntJogador):
                            pergunta = ["museu: ", "jardim: ", "abacaxi: ", "futebol: ", "janela: ", "professor: ", "paralelepípedo: ", "hipocondríaco: ", "sapato: ", "rinoceronte: ", "biblioteca: ", "psicólogo: "]

                            resposta = ["museu", "jardim", "abacaxi", "futebol", "janela", "professor", "paralelepípedo", "hipocondríaco", "sapato", "rinoceronte", "biblioteca", "psicólogo"]

                            jogador = jogador + 1
                            print("")
                            nome.append(input("    Jogador " + str(jogador) + " seu nome: "))
                            print("""
    Vamos começar! Aperte ENTER quando estiver pronto
                            """)
                            input()
                            tempo_inicial = time.time()

                            for q in range(qntPergunta):
                                Pergunta_sorteada = random.choice(pergunta)
                                resposta_digitada = input('    Digite a palavra ' + str(Pergunta_sorteada))
                                r_sorteada = pergunta.index(Pergunta_sorteada)
                                print("""
                                """)

                                while Pergunta_sorteada in pergunta: 
                                    pergunta.remove(Pergunta_sorteada)

                                    while not resposta_digitada == resposta[r_sorteada]:
                                        resposta_digitada = input('    Digite a palavra ' + str(Pergunta_sorteada)) 
                                        print("""
                                        """)

                                    if resposta_digitada == resposta[r_sorteada]:
                                        resposta.remove(resposta[r_sorteada])
                                        tempo_final = time.time() 
                                        continue

                            tempo_total = tempo_final - tempo_inicial

                            print('   ', nome[index], 'demorou', round(tempo_total, 1), 'segundos para responder as perguntas.')
                            index = index + 1            
                            tempos.append(float(tempo_total)) 
                            print("""
    Aguarde...
            """)
                            time.sleep(1)

                        podio = sorted(tempos)

                        if qntJogador == 2:

                            primeiro = tempos.index(podio[0])
                            segundo = tempos.index(podio[1])

                            print("     Parabéns", nome[primeiro], "você foi o ganhou.")
                            print('')
                            print("    ", nome[segundo], "você foi o segundo.")
                            print('')

                        else:
                            primeiro = tempos.index(podio[0])
                            segundo = tempos.index(podio[1])
                            terceiro = tempos.index(podio[2])

                            print("    Parabéns", nome[primeiro], "você ganhou.")
                            print('')
                            print("    ", nome[segundo], "você foi o segundo.")
                            print('')
                            print("    ", nome[terceiro], "você foi o terceiro.")
                            print('')

                        jogador = 0 
                        index = 0
                        nome = []
                        tempos = []

                        final = input("    Deseja jogar novamente(s/n): ")

                        if final == "s":
                            pass
                        elif final == "n": 
                            jogo = False
                              
                        else:
                            while True:
                                print('')
                                print("    Entrada invalida")
                                print('')
                                final = input("    Deseja jogar novamente(s/n): ")
                                if final == "s":
                                    break
                                elif final == "n":
                                    jogo = False
                                    break
                        time.sleep(3)
                    
                    
                    while modo != "2" or modo != "1":
                        print("""
    Entrada inválida. Tente novamente.""")
                        time.sleep(2)
                        break
                            
                

            # Configurações do jogo também está em loop, a pessoa pode alterar mais de uma configuração

            elif opção == "2":

                Config = True

                while Config == True:
                    print(""""
    ============= CONFIGURAÇÕES ============ 
            """)
                    print("""    Numero de jogadores atual:""",qntJogador,"""___________
                    """)
                    print("""    Numero de perguntas atual:""",qntPergunta,"""___________
                    
    -----------------------------------------
    """)
                    print("""    1 - Para mudar a quantidade de jogadores 
                    """)
                    print("""    2 - Para mudar a quantidade de perguntas 
                    """)
                    print("""    3 - Para mudar o idioma  _______________
                    """)
                    print("""    4 - Para voltar ao menu principal ______

    =========================================
    """)

                    Choice = input("    Digite a opção desejada: ")
                    print("")


                    if Choice == "1":
                        qntJogador = input("    Quantos vão jogar (min:2 ; max: 4)? ")
                        print("")
                        qntJogador = int(qntJogador)

                        while not 2 <= qntJogador <= 4:
                            qntJogador = input("    Quantos vão jogar (min:2 ; max: 4)? ")
                            print("")
                            qntJogador = int(qntJogador)
                        print("""
    Salvando...""")

                    elif Choice == "2":
                        qntPergunta = input("    Quantas perguntas por jogador (max:12)? ")
                        print("")
                        qntPergunta = int(qntPergunta)

                        while not 1 <= qntPergunta <= 12:
                            qntPergunta = input("    Quantas perguntas por jogador (max:12)? ")
                            print("")
                            qntPergunta = int(qntPergunta)
                        print("""
    Salvando...""")
                    
                    elif Choice == "3":
                        idioma = input("""    ========================================
                        
    1 - Português
    
    2 - Ingles

    Qual o idioma? """)
                        print("")

                        while not "1" <= idioma <= "2":
                            idioma = input("""    ========================================
    
    1 - Português

    2 - Inglês             

    Qual o idoma? """)

                        # caso a pessoa deseje mudar de idioma imediatamente o loop do menu e das configurações 
                        # é quebrado e o jogo reinicia na língua escolhida.
                        if idioma == "2":
                            print("""
    Changing language...""")
                            Menu = False
                            Config = False

                    elif Choice == "4":
                        Config = False

                    else:
                        while True:
                            print("    Entrada invalida ")
                            print("")
                            Choice = input("    Digite a opção desejada: ")
                            print("")


                            if Choice == "1":
                                qntJogador = input("    Quantos vão jogar? (min:2 ; max: 4): ")
                                print("")
                                while not 2 <= qntJogador <= 4:
                                    qntJogador = input("     Quantos vão jogar? (min:2 ; max: 4): ")
                                    print("")
                                print("""
    Salvando...""")
                                break

                            if Choice == "2":
                                qntPergunta = input("    Quantas perguntas por jogador? (max:12): ")
                                print("")
                                while not 1 <= qntPergunta <= 12:
                                    qntPergunta = input("    Quantas perguntas por jogador? (max:12): ")
                                    print("")
                                print("""
    Salvando...""")
                                break

                            if Choice == "3":
                                idioma = input("""    ========================================
    1 - Português

    2 - Ingles

    Qual o idoma? """)
                                print("")
                                while not "1" <= idioma <= "2":
                                    idioma = input("""    ========================================
    1 - Português

    2 - Ingles

    Qual o idoma? """)
                                    print("")
                                if idioma == "2":
                                    print("""
    Changing language...""")
                                    Menu = False
                                    Config = False
                                break

                            elif Choice == "4":
                                Config = False
                                break
                            else:
                                pass
                    time.sleep(1)


            # aqui é só um tutorial caso a pessoa não saiba jogar

            elif opção == "3":
                print("""
    ================ TUTORIAL =================

    Esse jogo possui dois modos, onde o jogador 
    pode escolher entre o modo digitação e o 
    modo matemática.
            """)
                time.sleep(5)

                print("""    No modo matemática, serão feitas perguntas 
    aleatórias com contas matemáticas e você 
    deve responder com o resultado da conta. 

    Exemplo:
      Quanto é 30+2?
      Qual o resultado de 6X9?
      Qual a raiz de 625?""")
                time.sleep(8)

                print("""
    Já no modo digitação, aparecerão palavras 
    aleatórias e você deve digitar a palavra.

    Exemplo:
      Digite a palavra casa:
      Digite a palavra porta:
      Digite a palavra noite:""")
                time.sleep(7)
                print("""
    Você deve responder as perguntas o mais 
    rápido possível, pois o seu tempo estará 
    sendo contabilizado. Ganha aquele que 
    responder  mais rápido.""") 
                time.sleep(6)
                print("""
    Nas configurações do jogo você pode escolher 
    quantos jogadores estarão participando, o 
    números de perguntas por rodada e o idioma. 

    Espero ter ajudado e bom jogo. """)
                input("""
    Aperte ENTER para voltar para o MENU""") 



            elif opção == "4":
                print("""    
    ========================================

            Esse jogo foi criado por: 

                    Esley

                    Raysa

                    Greg

    ========================================""") 
                input("""
    Aperte ENTER para voltar para o MENU""")


            # Saída

            elif opção == "5":
                print(""" 
          Você escolheu sair!
    Muito obrigado por participar do jogo. 
           Volte sempre! ^_^  """)
                time.sleep(3)
                Menu = False
                Lingua = False
                break

            # Mensagem de erro, reinicia o menu.
            
            else:
                print("""
    Opção invalida. Tente novamente.
    """)


    # Jogo em inglês:

    elif idioma == "2":
        print("""
    Loading...""")
        time.sleep(2)

        # Criei as variáveis em inglês pra ficar mais fácil de identificar

        qntPlayer = 2
        name = []
        times = []
        qntQuestion = 3
        player = 0
        index = 0
        
        print("""
    ==============  WELCOME  ==============
        This is a speed game of typing. 
     The game can be played by 2 or even 4 
     players, so you can call friends and 
     let's start playing.                    
    ========================================
            """)
        time.sleep(3)

        # A partir daqui o código é basicamente o mesmo, só que em inglês

        Menue = True

        while Menue == True:
        
        
            option = input("""
    ================= MENU =================

    1 - Game  ______________________________

    2 - Settings ___________________________

    3 - Tutorial ___________________________

    4 - Credits ____________________________

    5 - Quit _______________________________

    ========================================

    Enter which option you want: """)

            time.sleep(2)


            # Game

            if option == "1":
            
                game = True

                while game == True:
                
                    mode = input("""
    ========================================

    Choose which game mode:

    1 - Mathematics ________________________
    2 - Typing _____________________________

    ========================================

    Enter which option you want: """)

                    # Modo matemática:

                    if mode == "1":

                        for i in range(qntPlayer):
                            question = ["How much is 2+20? ", "How much is 4/2? ", "How much is 7-4? ", "How much is 8/2? ", "How much is 5x5? ", "How much is 9x9? ", "What is the root of 225? ", "What is the root of 64? ", "How much is 50+22? ", "How much is 15x3? ", "How much is 20x20? ", "How much is 40-2? "]

                            answer = ["22", "2", "3", "4", "25", "81", "15", "8", "72", "45", "400", "38"]

                            player = player + 1
                            print("")
                            name.append(input("    Player " + str(player) + " your name: "))
                            print("""
    Let's start! Press ENTER when ready
                            """)
                            input()
                            tempo_inicial = time.time()

                            for q in range(qntQuestion):
                                Question_sorted = random.choice(question)
                                answer_typed = input("    " + str(Question_sorted))
                                a_sorted = question.index(Question_sorted)
                                print("""
                                """)

                                while Question_sorted in question:
                                    question.remove(Question_sorted)

                                    while not answer_typed == answer[a_sorted]:
                                        answer_typed = input("    " + str(Question_sorted)) 
                                        print("""
                                        """)

                                    if answer_typed == answer[a_sorted]:
                                        answer.remove(answer[a_sorted])
                                        tempo_final = time.time() 
                                        continue

                            tempo_total = tempo_final - tempo_inicial

                            print('   ', name[index], 'took', round(tempo_total, 1), 'seconds to answer the questions.')
                            index = index + 1            
                            times.append(float(tempo_total)) 
                            print("""
    Loading...
            """)
                            time.sleep(1)

                        podio = sorted(times)

                        if qntPlayer == 2:

                            primeiro = times.index(podio[0])
                            segundo = times.index(podio[1])

                            print("    Congratulations", name[primeiro], "you won.")
                            print('')
                            print("    ", name[segundo], "you were the second.")
                            print('')

                        else:
                            primeiro = times.index(podio[0])
                            segundo = times.index(podio[1])
                            terceiro = times.index(podio[2])

                            print("    Congratulations", name[primeiro], "you won.")
                            print('')
                            print("    ", name[segundo], "you were the second.")
                            print('')
                            print("    ", name[terceiro], "you were the third.")
                            print('')

                        player = 0 
                        index = 0
                        name = []
                        times = []

                        finale = input("    Do you want to play again? (y/n): ")

                        if finale == "y":
                            pass
                        elif finale == "n": 
                            game = False
                        else:
                            while True:
                                print('')
                                print("    Invalid Input. Try again.")
                                print('')
                                finale = input("    Do you want to play again? (y/n): ")
                                if finale == "y":
                                    break
                                elif finale == "n":
                                    game = False
                                    break
                        time.sleep(3)


                    # Modo digitação:

                    elif mode == "2":
                        for i in range(qntPlayer):
                            question = ["museum: ", "garden: ", "pineapple: ", "football: ", "window: ", "teacher: ", "parallelepiped: ", "hypochondriac: ", "shoe: ", "rhinoceros: ", "library: ", "psychologist: "]

                            answer = ["museum", "garden", "pineapple", "football", "window", "teacher",  "parallelepiped", "hypochondriac", "shoe", "rhinoceros", "library", "psychologist"]

                            player = player + 1
                            print("")
                            name.append(input("    Player " + str(player) + " your name: "))
                            print("""
    Let's start! Press ENTER when ready
                            """)
                            input()
                            tempo_inicial = time.time()

                            for q in range(qntQuestion):
                                Question_sorted = random.choice(question)
                                answer_typed = input("    Type the word " + str(Question_sorted))
                                a_sorted = question.index(Question_sorted)
                                print("""
                                """)

                                while Question_sorted in question:
                                    question.remove(Question_sorted)

                                    while not answer_typed == answer[a_sorted]:
                                        answer_typed = input("    Type the word " + str(Question_sorted)) 
                                        print("""
                                        """)

                                    if answer_typed == answer[a_sorted]:
                                        answer.remove(answer[a_sorted])
                                        tempo_final = time.time() 
                                        continue

                            tempo_total = tempo_final - tempo_inicial

                            print('   ', name[index], 'took', round(tempo_total, 1), 'seconds to answer the questions.')
                            index = index + 1            
                            times.append(float(tempo_total)) 
                            print("""
    Loading...
            """)
                            time.sleep(1)

                        podio = sorted(times)

                        if qntPlayer == 2:

                            primeiro = times.index(podio[0])
                            segundo = times.index(podio[1])

                            print("    Congratulations", name[primeiro], "you won.")
                            print('')
                            print("    ", name[segundo], "you were the second.")
                            print('')

                        else:
                            primeiro = times.index(podio[0])
                            segundo = times.index(podio[1])
                            terceiro = times.index(podio[2])

                            print("    Congratulations", name[primeiro], "you won.")
                            print('')
                            print("    ", name[segundo], "you were the second.")
                            print('')
                            print("    ", name[terceiro], "you were the third.")
                            print('')

                        player = 0 
                        index = 0
                        name = []
                        times = []

                        finale = input("    Do you want to play again? (y/n): ")

                        if finale == "y":
                            pass
                        elif finale == "n": 
                            game = False
                        else:
                            while True:
                                print('')
                                print("    Invalid Input. Try again.")
                                print('')
                                finale = input("    Do you want to play again? (y/n): ")
                                if finale == "y":
                                    break
                                elif finale == "n":
                                    game = False
                                    break
                        time.sleep(3)


                    else:
                        while mode != "1" or mode != "2":
                            print("""
    Invalid Input. Try again. """)
                        time.sleep(2)
                        break



            # Configurações:

            elif option == "2":

                Sett = True

                while Sett == True:
                    print(""""
    =============== SETTINGS ================ 
            """)
                    print("""    Current number of players:""",qntPlayer,"""___________
                    """)
                    print("""    Current number of questions:""",qntQuestion,"""_________
                    
    -----------------------------------------
    """)
                    print("""    1 - To change the amount of players _____
                    """)
                    print("""    2 - To change the number of questions ___
                    """)
                    print("""    3 - To change the language  _____________
                    """)
                    print("""    4 - To go back to the main menu _________

    =========================================
    """)

                    Choice = input("    Enter which option you want: ")
                    print("")

                    if Choice == "1":
                        qntPlayer = input("    How many will play? (min:2 ; max:4): ")
                        print("")
                        qntPlayer = int(qntPlayer)

                        while not 2 <= qntPlayer <= 4:
                            qntPlayer = input("    How many will play? (min:2 ; max:4): ")
                            print("")
                            qntPlayer = int(qntPlayer)
                        print("    Saving...")
                        time.sleep(2)

                    elif Choice == "2":
                        qntQuestion = input("    How many questions per player (max:12)? ")
                        print("")
                        qntQuestion = int(qntQuestion)

                        while not 1 <= qntQuestion <= 12:
                            qntQuestion = input("    How many questions per player (max:12)? ")
                            print("")
                            qntQuestion = int(qntQuestion)
                        print("    Saving...")
                        time.sleep(2)

                    elif Choice == "3":
                        idioma = input("""    ========================================
    
    1 - Portuguese

    2 - English
                                            
    Witch language? """)
                        print("")

                        while not "1" <= idioma <= "2":
                            idioma = input("""    ========================================    
    
    1 - Portuguese

    2 - English
                                            
    Witch language? """)
                            print("")

                        # Aqui muda o jogo imediatamente para português:
                        if idioma == "1":
                            print("""
    Mudando de idioma...""")
                            time.sleep(3)
                            Menue = False
                            Sett = False

                    elif Choice == "4":
                        Sett = False

                    else:
                        while True:
                            print("    Invalid Input. Try again. ")
                            print("")
                            Choice = input("    Enter which option you want: ")
                            print("")

                            if Choice == "1":
                                qntPlayer = input("    How many will play? (min:2 ; max:4): ")
                                print("")
                                qntPlayer = int(qntPlayer)

                                while not 2 <= qntPlayer <= 4:
                                    qntPlayer = input("     How many will play? (min:2 ; max:4): ")
                                    qntPlayer = int(qntPlayer)
                                print("    Saving...")
                                time.sleep(2)
                                break

                            if Choice == "2":
                                qntQuestion = input("    How many questions per player (max:12)? ")
                                print("")
                                qntQuestion = int(qntQuestion)

                                while not 1 <= qntQuestion <= 12:
                                    qntQuestion = input("    How many questions per player (max:12)? ")
                                    print("")
                                    qntQuestion = int(qntQuestion)
                                print("    Saving...")
                                time.sleep(2)
                                break

                            if Choice == "3":
                                idioma = input("""    ========================================
    
    1 - Portuguese

    2 - English             

    Witch language? """)
                                print("")

                                while not "1" <= idioma <= "2":
                                    idioma = input("""    ========================================
                                    
    1 - Portuguese

    2 - English
                                            
    Witch language? """)
                                    print("")

                                if idioma == "1":
                                    Menue = False
                                    Sett = False
                                    print("""
    Mudando de idioma...""")
                                    time.sleep(3)
                                break

                            elif Choice == "4":
                                Sett = False
                                break

                            else:
                                pass
                    time.sleep(1)



    # Tutorial:
            
            elif option == "3":
                print("""
    =============== TUTORIAL ================

     This game has two modes, where the player
     can choose between typing mode and
     math mode. 
            """)
                time.sleep(5)

                print("""     In math mode, random questions will be 
     asked with math accounts and you
     must respond it with the result of the 
     account. 

     Example:
        How much is 30+2?
        How much is 6X9?
        What is the root of 625?""")
                time.sleep(8)

                print("""
     In typing mode, random words will
     appear and you must type the word.

     Example:
        Type the word home:
        Type the word door:
        Type the word night:""")
                time.sleep(7)
                print("""
     You must answer the questions as quickly 
     as possible, because your time will be
     counting. The person that answers the 
     questions faster wins.""") 
                time.sleep(6)
                print("""
     In game settings you can choose how many 
     players will be participating, the number 
     of questions per round and the language. 

     Hope I helped and good game.""")
                input("""
    Press ENTER to return to MENU""")



            elif option == "4":
                print("""    
    ========================================

            This game was created by:

                    Esley

                    Raysa

                    Greg
                
    ========================================""") 
                input("""
    Press ENTER to return to MENU""")


            # Saída:
            elif option == "5":
                print(""" 
                You chose to leave!
    Thank you so much for participating in the game.
              Check back often! ^_^ """)
                time.sleep(3)
                Menue = False
                Lingua = False

            else:
                print("""
    Invalid option. Try again.
    """)   
