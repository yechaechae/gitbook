## Implementing Heap Files 
heapfile은 create, destory, insert a record, delete a record with a given rid, get a record with a given rid

## CH9 
* 디스크 모델링
    * 메모리 계층
    * DBMS가 disk 공간을 manage 하는 법
    * DBMS가 데이터를 disk에서 memory로 보낸느 법
    * page의 collection이 heap file안에 organized 되는 법

### Memory Hierarchy
permanat 한 데이터는 second에 저장 

페이지를 요청했는데 그 페이지가 buffer pool에 없으면 다른 free frame을 정한다.
만약에 frame이 dirty하면 disk에 쓴다.
선택한 frame으로 요청 된 페이지를 읽는다 ??????

address를 반환 할 때 페이지를 pin한다.
page요청자는 반드시 그것??을 unpin을 해야하고 page가 수정되었는지 표시해야한다.
dirty bit이 이때 사용된다.

pin count를 record해야 함
pin count가 0이면 replacement의 후보 페이지.

