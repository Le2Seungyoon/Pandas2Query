# Pandas2Query
Pandas는 데이터 분석 및 조작을 위한 굉장히 편리한 패키지이지만,   
이를 DB에서 바로 사용할 수 없다는 단점이 있습니다.   
그렇다고 DB를 Python 환경으로 업로드 후 Pandas를 사용하는 것은 비효율적입니다.   
따라서 업무 중 Pandas에서 빈번하게 활용하는 메서드들을 쿼리로 제시하여,  
Python 사용자들의 SQL 능력을 향상시키고자 합니다.  

## Index
```
sample  
├── data.csv         
├── total.ipynb           
│   ├── data         
│   └── data.columns                 
├── column.ipynb  
│   ├── data['column']
│   ├── data['column'].dtype              
│   ├── data['column'].unique()
│   ├── data['column'].nunique()
│   ├── data['column'].value_counts()
│   └── data['column'].value_counts(normalize=True)
├── nan.ipynb  
│   ├── data['column'].isnull().sum()                
│   ├── data[data['column'].isna()]
│   └── data[~data['column'].isna()]                         
└── statistics.ipynb        
    └── data['column'].describe()
```
4개의 .ipynb 파일은 각각 다음 4가지에 대해서 다루고 있습니다.  
1) [전체 데이터를 탐색할 경우](https://github.com/Le2Seungyoon/Pandas2Query/blob/main/sample/total.ipynb)
2) [데이터에서 특정 컬럼을 탐색할 경우](https://github.com/Le2Seungyoon/Pandas2Query/blob/main/sample/column.ipynb)
3) [결측값에 대해서 탐색할 경우](https://github.com/Le2Seungyoon/Pandas2Query/blob/main/sample/nan.ipynb)
4) [통계량을 구하는 경우](https://github.com/Le2Seungyoon/Pandas2Query/blob/main/sample/statistics.ipynb)

각각에 대해서는 링크를 참고 부탁드립니다.  
