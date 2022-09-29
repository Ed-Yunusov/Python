1) Открыть страницу https://opensource-demo.orangehrmlive.com/ и написать тест для логина в систему.
```py
import time 
from selenium import webdriver # Импортируем webdriver (набор команд для управления браузером)
driver = webdriver.Chrome(executable_path='C:/chromedriver.exe') # Вызываем драйвер браузера
driver.maximize_window() # Открываем браузер в полном окне
driver.get("https://opensource-demo.orangehrmlive.com/") # Сообщаем браузеру, что нужно открыть сайт по указанной ссылке
time.sleep(3) # Устанавливаем паузу в 3 секунды
login = driver.find_element_by_name("username") # Объявляем переменную login, задаём ей значение селектора поля логин
login.send_keys("Admin") # Вводим логин в поле
password = driver.find_element_by_name("password") # Объявляем переменную password, задаём ей значение селектора поля пароль
password.send_keys("admin123") # Вводим пароль в поле
login_btn = driver.find_element_by_css_selector(".oxd-button") # Объявляем переменную login_btn, задаём ей значение селектора кнопки логин
login_btn.click() # Кликаем на элемент
driver.quit() # Закрываем все вкладки и завершаем процесс webdriver
```
