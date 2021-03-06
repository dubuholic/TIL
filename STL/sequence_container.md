# 시퀀스 컨테이너  

## string   
push_back() : O(1)     
[] > at() : O(1)  
배열 구조   
배열 구조라 push_back()이 아닐 경우 뒤에 있는 항목을 밀어내야 함 : O(n)  
정렬 : O(nlogn)  
iterator 검색 : O(n) / 정렬되어 있다면 O(logn)    

## vector   
push_back() : O(1)      
[] > at() : O(1)   
배열 구조   
배열 구조라 push_back()이 아닐 경우 뒤에 있는 항목을 밀어내야 함 : O(n)   
정렬 : O(nlogn)  
iterator 검색 : O(n) / 정렬되어 있다면 O(logn)   

## deque    
push_back() : O(1)   
push_front() : O(1)  
[] > at() : O(1)  
배열 구조라 push_back()이 아닐 경우 뒤에 있는 항목을 밀어내야 함   
정렬 : O(nlogn)  
iterator 검색 : O(n) / 정렬되어 있다면 O(logn)   
데큐에서 수행하는 모든 연산의 비례 상수는 벡터보다 큼 (즉. 벡터보다 성능이 느리다)   

## list  
push_back() : O(1)   
push_front() : O(1)  
중간에 항목을 삽입해도 O(1)  
정렬 : O(nlogn)  
검색시간 항상 O(n) / 첨자나 at 제공하지 않음   
리스트 항목을 복사하지 않고 O(1) 시간에 특정 범위 항목을 추출하거나 병합 가능 => 목록을 만든 다음 순서를   뒤섞는다면 벡터보다 유리   

## forward_list  
push_front() : O(1)     
중간에 항목을 삽입해도 O(1)  
정렬 : O(nlogn)    
검색시간 항상 O(n) / 첨자나 at 제공하지 않음   
메모리를 효율적으로 관리할 수 있으며 메모리 단편화가 생길 가능성이 적지만 속도는 빠르지 않다.  

# 결론  
대부분의 경우에 일단 vector를 들이대자.   