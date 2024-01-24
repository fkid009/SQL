# SQL
MySQL을 공부하기 위한 목적으로 내용을 정리하고 있습니다.
실습에 사용된 데이터는 공개해드릴 순 없지만, MySQL은 직관적으로 코드가 구성되어 있어 충분히 이해할 수 있을 것으로 예상됩니다.

# Why SQL?
데이터 사이언티스트는 데이터를 수집하고 분석하여 비즈니스 문제를 해결하고 의사결정을 내리는 전문가를 의미합니다.
따라서, 시각화, 머신러닝 등 다양한 도구를 사용하여 데이터 내에 존재하는 규칙이나 특성을 찾아내는 것이 중요합니다.

하지만 이러한 상황에서, 데이터에 대해 제대로 이해하고 있지 않으면 만들어낼 수 있는 인사이트는 제한적일 수 밖에 없습니다.

그 외에도, 데이터의 구조에 대해 잘 알고있으면 데이터를 요청하고 받는 과정에서 혼선을 줄이고 원하는 데이터만 골라서 빠르게 요청할 수 있습니다. 또한, 데이터로부터 가설을 설정할 때, 데이터 유무를 빠르게 인지하고 결과를 도출할 수 있습니다.

# What is SQL?
데이터를 이해하기 위해서는 데이터를 저장하는 Database와 데이터를 다루는 언어인 SQL을 알아야 합니다.

먼저, SQL은 "Structured" Query Language의 약자로서, 구조화된 질문을 던지는 언어를 의미합니다.
이때, 구조화된 데이터는 일정한 체계를 가지고 논리적으로 가공된 정보를 의미합니다.

현재 데이터를 관리하는 여러가지 툴이 존재합니다. 대표적으로, 엑셀은 개인이 작업하기 최적화된 형태로 데이터를 정리해서 보기 편리하고 함수를 통해 다양한 작업이 가능하다는 장점이 존재합니다. 하지만, 엑셀은 특정 개인이 보기 쉽도록 데이터가 구성되어 있기 때문에, 공유해서 작업하기 힘들고 서로 다른 데이터를 보고 있을 가능성이 높으며 낮은 처리 속도를 보여준다는 단점이 존재합니다.

따라서, 실제 현업에서 서비스를 제공하기 위해서는 빠른 처리 속도와 많은 인원들이 데이터를 함께 효율적으로 다루기 위해 Database를 사용하게 됩니다. 

Database에는 여러가지 방식이 있지만, 자주 사용되는 방식은 "Relational" Database 즉, 관계형 데이터베이스입니다. 
왜 관계형이라는 명칭이 붙었을까요?
이는 데이터베이스에 보관된 테이블끼리 특정한 관계를 가지고 있기 때문입니다.

예를 들어, 아래와 같이 Orders라는 주문 데이터가 있다고 가정해봅시다.
이를 사용해서 어떤 인사이트를 도출하고 싶을때, Orders에 있는 모든 데이터를 사용하지 않아도 되거나, 해당 소비자와 아이템의 정보를 바꿔야될 상황이 발생할 수 있습니다.
하지만, 만약 Orders라는 데이터만 존재한다면, 필요없는 데이터를 불러와야되고 데이터의 정보를 변경하는데 행별로 바꿔줘야한다는 비효율적인 상황이 발생합니다. 

따라서, 공통 키를 기준으로 Orders와 더불어 소비자의 정보가 담긴 테이블, 아이템의 정보가 담긴 테이블 등 테이블을 나눠주는 것이 효율적일 것입니다. 
즉, 이처럼 테이블 간의 특정 관계로 묶여져 데이터베이스를 형성하는 것이 Relational Database입니다. 
<img src="https://planetscale.com/_next/image?url=%2Fassets%2Fblog%2Fcontent%2Fschema-design-101-relational-databases%2Fdb72cc3ac506bec544588454972113c4dc3abe50-1953x1576.png" width="100" height="100"/>




