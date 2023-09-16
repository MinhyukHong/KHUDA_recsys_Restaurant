경희대 맛집 추천해드립니다: 다양한 플랫폼 데이터를 활용한 장소 개인화 맞춤 시스템<br>
We recommend good restaurants at Kyunghee University! : Location-type Personalization Recommendation System Using Various Platform Data
======================================================================================
프로젝트 소개 Our Project
----------------------
![image](https://github.com/MinhyukHong/RecSys_Restaurant/assets/108979014/f908c309-266a-4212-922a-741108768c4b)
당신이 맛집에 관심이 높다면, 맞춤형 자세한 정보를<br>
If you're interested in a good restaurant, you can get more customized information

당신이 맛집에 관심이 낮다면, 임의의 간단한 정보를<br>
If you're not interested in good restaurants, you can use any simple information

당신이 있는 지역이 새로운 지역이라면, 대중적으로 인기 있는 장소를<br>
If you're in a new area, you're going to find a popular place

당신이 있는 지역이 익숙한 지역이라면, 숨겨져 있던 새로운 장소를<br>
If you're familiar with the area, you can find a new hidden location

지역, 거리와 같은 “상황적 맥락”과 가성비, 맛 분위기와 같은 “취향”까지 사로잡는 장소 개인화 맞춤 시스템을 소개합니다.<br>
We introduce a place personalization system that captures "situal context" such as region and street, as well as "taste" such as cost-effectiveness, taste and mood.
<hr/>

 ## Introduction
<img width="739" alt="무제" src="https://github.com/MinhyukHong/RecSys_Restaurant/assets/108979014/90880ec1-b630-4d78-9008-918b6730d932">
학교를 다닌지 3년째여도 여전히 매번 식사 메뉴를 고민하게 됩니다. 이는 매번 밥을 먹는 상황이 달라지고, 취향이 달라지기 때문입니다.<br>
Even if it's been three years since we stayed in Kyunghee University, we still think about the menu every time. This is because the situation of eating each meal changes and the taste changes.

하지만 우리가 밥을 먹을 때마다 누구와, 언제, 무엇을 먹었는지 유튜브 시청기록처럼 남겨지지 않습니다.<br>
But every time we eat, who, when, and what we ate are not left like YouTube viewing records.

개인화 장소 추천의 핵심은 여기에 있습니다. 우리의 기록은 남겨지지도 않지만, 상황이 매번 달라지기 때문에 기록의 중요성이 떨어집니다.<br>
Here's the key to recommending a personalized place. Our records are not even kept, but they are less important because things change every time.


과거의 기록에 치중되었던 기존의 추천에서 나아가, 과거와 현재의 조화를 이뤄내고자 하였습니다.<br>
We tried to achieve harmony between the past and the present, going beyond the existing recommendations that were focused on the past record.
<hr/>

## Members
• 노명은 Myeongeun No<br>
• 홍민혁 Minhyuk Hong<br>
• 서지은 Jieun Seo
<hr/>

## Data
![image](https://github.com/MinhyukHong/RecSys_Restaurant/assets/108979014/96d34226-e74a-4662-96ed-d91d25fb785a)

모든 데이터는 웹 크롤링을 통해 수집하였습니다. 크게 3가지 웹사이트에서 수집했습니다.<br>
All the data was collected through web crawling. It was collected from three websites.

• 네이버 플레이스 : 특정 키워드 검색 결과 페이지에서 가게별로 정보 수집<br>
Naver Place: Collect information by restaurant on the search result page for specific keywords

• 인스타그램 : 특정 계정 페이지에서 해시태그와 게시글 정보 수집<br>
Instagram: Gather hashtags and posts information from specific account pages

• 망고플레이트 : 특정 키워드 검색 결과 페이지에서 가게별로 정보 수집<br>
Mango Plate: Gather information by restaurant on the search result page for specific keywords
<hr/>

## 핵심 기능 How does it work?
과거를 담아내기 위해 사용자의 맛집 관심도, 장소 방문 빈도, 선택 기준을 고려합니다.<br>
To include the past, consider your interest in restaurants, frequency of place visits, and selection criteria.

현재를 담아내기 위해 현재 위치, 인원, 메뉴, 여러 상황 맥락을 담은 키워드를 고려합니다.<br>
To include the present, consider keywords with current location, number of people, menus, and different context.

### 과거: USER의 관심도, 장소 방문 빈도, 선택 기준
![image](https://github.com/MinhyukHong/RecSys_Restaurant/assets/108979014/efac776d-f75a-4271-9f32-0ba1c20794e6)

추천 알고리즘은 크게 사용자 그룹에 따라 달라집니다. 맛집 관심도가 높은 사용자에게는 개인화 추천 위주의 자세한 추천(망고플레이트 요약 리뷰 및 가게 상세 정보), 그렇지 않은 사용자들은 임의성이 반영된 인기도 위주의 추천(인스타그램 해시태그 바탕의 워드 클라우드)이 제공됩니다.<br>
Recommendation algorithms largely depend on user groups. Users who are interested in restaurants will be given detailed recommendations focused on personalization recommendations (mango plate summary review and restaurant details), and those who are not will be given popular recommendations based on randomness (word cloud based on 
Instagram hashtag).

![image](https://github.com/MinhyukHong/RecSys_Restaurant/assets/108979014/989a7d5c-173f-45fc-a241-6e95e3d5859a)

다음으로는 장소 방문 빈도를 고려합니다. 처음 등록했던 자주 가는 지역이, 현재 추천을 받고자 하는 지역과 일치한다면 개인화가 더 반영된, 혹은 새로운 장소의 추천을 제공합니다.<br>
Next, consider the frequency of place visits. If the first frequented area you registered matches the area you are currently looking for recommendations, it will provide recommendations for new places with more personalization.

![image](https://github.com/MinhyukHong/RecSys_Restaurant/assets/108979014/d85131b5-00ee-4409-afde-aa81ad04ed11)

만약 일치하지 않는다면, 대중적으로 인기있는 장소를 추천해줍니다.<br>
If it doesn't match, it'll recommend a popular place.
<hr/>

## 현재: 위치, 인원, 메뉴, 상황, 키워드 Present: location, number of people, menu, situation, keyword
과거의 정보를 바탕으로 우선 장소를 선별한 다음, 현재 상황에 대한 정보로 필터링을 해 최종적으로 장소 추천을 제공합니다.<br>
Based on past information, we select places first, and then filter them with information about the current situation to finally provide recommendations for places.

현재 상황으로는 선호하는 음식 종류(한식, 일식, 양식 … ), 거리, 상황 키워드(인원 등)를 고려합니다.<br>
As of now, the type of food you prefer (Korean food, Japanese food, Western food... ), distance, and context keywords (people, etc.) are considered.

![image](https://github.com/MinhyukHong/RecSys_Restaurant/assets/108979014/ea8f4410-0ec9-4841-a840-3c3110795845)
<hr/>

## Reference
• [2023 Deview 상황에 맞는 취향 장소 발견하기. HyperLocal 추천 시스템 A to Z (Finding a place that suits your taste)](https://deview.kr/2023/sessions/553)<br>
• [2020 Deview 당신 취향의 맛집을 추천해드립니다 : 장소 개인화 추천 시스템의 비밀 (The Secret of the Place Personalization Recommendation System)](https://deview.kr/data/deview/session/attach/1600_T1_%EC%A0%84%EC%98%81%ED%99%98_%EB%8B%B9%EC%8B%A0%20%EC%B7%A8%ED%96%A5%EC%9D%98%20%EB%A7%9B%EC%A7%91%EC%9D%84%20%EC%B6%94%EC%B2%9C%ED%95%B4%EB%93%9C%EB%A6%BD%EB%8B%88%EB%8B%A4_%EC%9E%A5%EC%86%8C%20%EA%B0%9C%EC%9D%B8%ED%99%94%20%EC%B6%94%EC%B2%9C%EC%8B%9C%EC%8A%A4%ED%85%9C%EC%9D%98%20%EB%B9%84%EB%B0%80.pdf)<br>
• [크롤링 참고 자료 (Crawling References)](https://velog.io/@jahommer/%EB%84%A4%EC%9D%B4%EB%B2%84-%EB%A7%B5-%ED%81%AC%EB%A1%A4%EB%A7%81-seleniumbs4re-%ED%82%A4%EC%9B%8C%EB%93%9C-%EB%A6%AC%EB%B7%B0)


