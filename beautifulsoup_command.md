# beautifulsoup command  

```python
soup.title # title 정보 출력
soup.a # soup 객체에서 처음 발견되는 a element 반환
soup.arrts # 태그 속성 정보 출력
soup.a['href'] # a태그 href 속성 값 정보 출력
soup.find('a', attrs={'class':'클래스명 입력'}) # a 태그에 있는 특정 클래스 출력
soup.find(attrs={'class':'클래스명 입력'}) # 해당 클래스가 유일하면 태그명 제외 가능

var1 = soup.find(attrs={'class':'클래스명 입력'})
print(var1.a) # a 정보만 출력
var2 = var1.next_sibling.next_sibling # 부모 태그에서 자식 태그로 이동
var3 = var2.next_sibling.next_sibling # 부모 태그에서 자식 태그로 이동
print(var3.a.get_text())
var2 = var3.previous_sibling.previous_sibling # 이전 태그로 이동

var2 =  var1.find_next_sibling('li') # 바로 li 태그 찾기
print(var2.a.get_text())
var2 = var3.find_previous_sibling('li')
print(var2.a.get_text())

var1.find_next_siblings('li') # li 태그의 형제 태그 모두 가져오기

var = soup.find('a', text='독립일기') # a에서 해당 텍스트가 있는 정보 출력 
var = soup.find_all('a', attrs={'class':'클래스명 입력'}) # 해당 클래스 전체 출력
```

