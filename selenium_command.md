```python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.alert import Alert
from selenium.webdriver.common.action_chains import ActionChains

driver = webdriver.Chrome('driver 경로')
driver.get('크롤링할 주소')

driver.find_element(By.ID, '')
driver.find_element(By.XPARH, '')
driver.find_element(By.CLASS_NAME, '')
driver.find_element(By.NAME, '')
driver.find_element(By.TAG_NAME, '')
driver.find_element(By.LINK_TEXT, '')
driver.find_element(By.CSS_SELECTOR, '')

driver.find_element_by_name('query').send_keys('서울역') # 텍스트 입력
driver.find_element_by_name("query").send_keys(Keys.ENTER)
driver.find_element_by_name("query").clear() # 텍스트 삭제


#경고창으로 이동
driver.switch_to.alert
Alert(driver).accept()    #경고창 수락 누름
Alert(driver).dismiss()   #경고창 거절 누름
print(Alert(driver).text  # 경고창 텍스트 얻음
      
driver.execute_script('window.scrollTo(0, document.body.scrollHeight)') # 스크롤 가장 아래로 내리기
      
             
actions = ActionChains(driver).move_to_element(element) \ # 마우스 이동
.click() # 마우스 클릭

actions.perform() # ActionChains 실행
      
```

