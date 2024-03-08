# bjdong-downloader

## Abstract
    bjdong.sh - 행정표준관리시스템에서 법정동 코드와 법정동 이름을 불러오는 스크립트
    
## SYNOPSIS
    sh ./bjdong.sh [--filter "FILTER_EXPRESSION"]

## DESCRIPTION
    'bjdong.sh'는 행정표준관리시스템을 통해 법정동 코드와 법정동 이름을 조회하고 필터링하는 쉘 스크립트입니다. 
    사용자는 특정 필터 조건을 설정하여 관심 있는 법정동의 데이터만을 추출할 수 있습니다. 
    이 스크립트는 데이터 분석, 정보 시각화, 지역 기반 서비스 개발 등 다양한 목적으로 활용될 수 있습니다.

## OPTIONS
    --filter "FILTER_EXPRESSION"
        사용자가 지정한 필터 조건을 적용합니다. 이 옵션은 큰따옴표(") 안에 필터링하고자 하는 조건을 문자열 형태로 지정해야 합니다. 
        예를 들어, 서울특별시 종로구에 해당하는 데이터만 필터링하고자 할 때는 --filter "서울특별시 종로구"와 같이 지정합니다.

## EXAMPLES
    일반 사용 예:
        sh ./bjdong.sh

    필터 조건을 사용하는 예:
        sh ./bjdong.sh --filter "서울특별시 종로구"

    이 스크립트는 필터 조건을 사용하여 사용자가 원하는 특정 데이터를 추출할 때 유용합니다.

## OUTPUT
    출력 결과는 output 이라는 디렉터리에 bjdong-{timestamp}.csv 형태로 저장됩니다.
    csv 의 컬럼은 차례대로 법정동코드(code), 법정동명(csv), 존재여부(etc) 입니다.
