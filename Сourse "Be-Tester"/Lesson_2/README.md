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
2) Открыть страницу https://opensource-demo.orangehrmlive.com/ и написать тест для создания пользователя.
```py
import time
from selenium import webdriver
driver = webdriver.Chrome(executable_path='C:/chromedriver.exe')
driver.maximize_window()
driver.get("https://opensource-demo.orangehrmlive.com/")
time.sleep(3)
login = driver.find_element_by_name("username")
login.send_keys("Admin")
password = driver.find_element_by_name("password")
password.send_keys("admin123")
login_btn = driver.find_element_by_css_selector(".oxd-button")
login_btn.click()
time.sleep(3)
Add_Employee = driver.find_element_by_link_text('Add Employee')
Add_Employee.click()
time.sleep(3)
First_name = driver.find_element_by_name('firstName')
First_name.send_keys("John")
Last_name = driver.find_element_by_name("lastName")
Last_name.send_keys("Doe")
Save_btn= driver.find_element_by_css_selector('.oxd-button--secondary')
Save_btn.click()
driver.quit()
```
3) Открыть страницу https://opensource-demo.orangehrmlive.com/ и написать тест для удаления пользователя.
```py
import time
from selenium import webdriver
driver = webdriver.Chrome(executable_path='C:/chromedriver.exe')
driver.maximize_window()
driver.get("https://opensource-demo.orangehrmlive.com/")
time.sleep(3)
login = driver.find_element_by_name("username")
login.send_keys("Admin")
password = driver.find_element_by_name("password")
password.send_keys("admin123")
login_btn = driver.find_element_by_css_selector(".oxd-button")
login_btn.click()
time.sleep(3)
Employee_id = driver.find_element_by_css_selector("div:nth-child(2) > input")
Employee_id.send_keys("0260")
time.sleep(3)
Search_btn = driver.find_element_by_css_selector(".orangehrm-left-space")
Search_btn.click()
time.sleep(3)
Delete_btn = driver.find_element_by_css_selector(".bi-trash")
Delete_btn.click()
time.sleep(3)
Yes_btn = driver.find_element_by_css_selector(".oxd-button--label-danger")
Yes_btn.click()
driver.quit()
```
