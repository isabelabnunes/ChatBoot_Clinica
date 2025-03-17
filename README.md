import os

def processar_resposta(resposta,nome):
    if resposta == '1':
        print(f'{os.linesep} Segunda-feira: (10:00);(10:50);(12:10) / Quarta-feira: (7:30);(9:15) / Sabado: (7:00);(9:40){nome}{os.linesep}')
    elif resposta == '2':
        print(f'{os.linesep}{nome} Entre em contato pelo telefone (75)3333-9633 ou (75)3535-6935{os.linesep}')
    elif resposta == '3':
        print(f'{os.linesep}{nome} Atendemos nas seguintes unidade: -Shopping Paralela -Shopping Bela Vista -Lauro de Freitas Horarios: Das 7:00 às 18:00 / de segunda a sabado{os.linesep}')
    elif resposta == '4':
        print(f'{os.linesep}{nome} Atendemos convenios: Sulamerica / Planserve / Amil / Bradesco /Unimed ou Particular / Aceitamos Pix, Débito ou Crédito{os.linesep}')
    else:
        print('Digite somente uma das opções 1, 2, 3 ou 4')


def start():
    #Apresentar o chat bot
    print('Olá! Seja bem vindo a Clinica Fisioclin, aqui Cuidamos do seu movimento, transformando sua saúde.')
    #pedir o nome
    nome = input('Digite seu nome completo:   ')
    #pedir o email
    email = input('Digite seu email:   ')
    while True:
        #oferecer as opções
        resposta = input(f'Selecione uma opção que melhor atenda voce:{os.linesep}[1] - Exibir horários disponíveis{
                    os.linesep}[2] - Reagendar ou cancelar consultas{
                    os.linesep}[3] - Informar endereço e horário de funcionamento{
                    os.linesep}[4] - formas de pagamento aceitas{
                    os.linesep}') 
    #Processar a resposta enviada
        processar_resposta(resposta,nome)

if __name__ == '__main__':
    start()
