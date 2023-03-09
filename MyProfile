indent = '--------------------------------'
finish = 'Завершение'
print('Приложение «MyProfile».\nСохраняй информацию о себе и выводи ее в разных формах.\n')

def telephone ():
  while True:
    value = input('Введите номер телефона(+7XXXXXXXXXX): ')
    if len(value) == 12:
      if value[0:2] == '+7':
        if value[2:12].isdigit():
          return value
        else:
          print('Неправильный номер')
      else:
        print('Неправильно введены данные. Начните с "+7"')
    else:
      print('Неправильно введены данные. Должно быть 12 символов')

def int_input_handler(value_name, digit_amount):
    while True:
        value = input(f'Введите {value_name} : ')
        if digit_amount == 0:
          if value.isdigit():
            return int(value)
        elif value.isdigit() and len(value) == digit_amount: 
            return int(value)
        
        print(f'Неправильно введены данные: {value_name}') 

def menu_2(pers_data, entrepreneur_data):
    while True:
      start_2 = int(input(f'{indent}\nВЫВЕСТИ ИНФОРМАЦИЮ \n1 — Общая информация\n2 — Вся информация\n0 — Назад\nВведите номер пункта меню: '))
      
      if start_2 == 1:
       
        if len(pers_data) != 0:
          print(f'\nИмя: {pers_data[0]}\nВозраст: {pers_data[1]}\nТелефон: {pers_data[2]}\nЕ-mail: {pers_data[3]}\nИндекс: {pers_data[4]}\nАдрес: {pers_data[4]}')
       
        else:
          print('\nВы не ввели данные')
      
      elif start_2 == 2:
        if len(entrepreneur_data) != 0 and len(pers_data) != 0:
          print(f'Информация о предпринимателе\n\nИмя: {pers_data[0]}\nВозраст: {pers_data[1]}\nТелефон: {pers_data[2]}\nЕ-mail: {pers_data[3]}\nИндекс: {pers_data[4]}\nАдрес: {pers_data[4]} ОГРНИП: {entrepreneur_data[0]}\nИНН: {entrepreneur_data[2]}\nБанконвские реквизиы \nР/с: {entrepreneur_data[3]}\nБанк: {entrepreneur_data[4]}\nБИК: {entrepreneur_data[5]}\nК/с: {entrepreneur_data[6]}')

        else:
          print('\nВы ввели не все данные')

      elif start_2 == 0:
        break
      
      else:
        print('Неправильная комбинация, попробуйте еще раз.')
        
def menu_1b():
  entrepreneur_data = []
  entrepreneur_data.append(int_input_handler('ОГРНИП', 15))
  entrepreneur_data.append(int(input('Введите ИНН: ')))
  entrepreneur_data.append(int_input_handler('расчетный счет', 20))
  entrepreneur_data.append(input('Введите название банка: '))
  entrepreneur_data.append(int_input_handler('БИК', 6))
  entrepreneur_data.append(int(input(' корресподентский счет: ')))
  return entrepreneur_data
        
def menu_1a():
  pers_data = []
  pers_data.append(input('Введите имя:'))
  pers_data.append(int_input_handler('возраст', 0))
  pers_data.append(telephone())
  pers_data.append(input('Введите адрес электронной почты: '))
  pers_data.append(int_input_handler('почтовый индекс', 6))
  pers_data.append(input('Введите почтовый адрес(без индекса): '))
  pers_data.append(input('Введите дополнительную информацию: '))
  return pers_data


def menu_1(pers_data, entrepreneur_data):
  while True:
    start_1 = int(input(f'{indent}\nВВЕСТИ ИЛИ ОБНОВИТЬ ИНФОРМАЦИЮ\n1 — Личная информация\n2 — Информация о предпринимателе\n0 — Назад\nВведите номер пункта: '))
    if start_1 == 1:
      pers_data = menu_1a()
    elif start_1 == 2:
      entrepreneur_data = menu_1b()
    elif start_1 == 0:
      return pers_data, entrepreneur_data
    else:
      print('Неправильная комбинация, попробуйте еще раз.')

def programma():
  pers_data = []
  entrepreneur_data = []
  while True:
    start = int(input(f'{indent}\nГЛАВНОЕ МЕНЮ \n1 — Ввести или обновить информацию\n2 — Вывести информацию\n0 — Завершить работу\n \nВведите номер пункта меню: '))
    if start == 1:
      pers_data, entrepreneur_data = menu_1(pers_data, entrepreneur_data)
    elif start == 2:
      menu_2(pers_data, entrepreneur_data)
    elif start == 0:
      print(finish)
      break
    else:
      print('Введён некорректный пункт меню, попробуйте снова')

programma()
