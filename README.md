sci-news-sum-kr-50
==========

네이버 뉴스 중 IT/과학 분야에서 50개를 선정해서 요약에 해당하는 문장을 태깅해둔 데이터셋입니다.

파일 한개당 뉴스 하나를 뜻하며, 원본 출처가 기록되어 있습니다. 비상업적인 실험에만 사용해주세요.

프리프로세싱을 어느정도 했으나, 가끔 정확하지 않은 문장 구분이나 이상한 말이 끼어있을 수 있습니다. 수정은 PR로 부탁드립니다.

'요약에 해당하는 문장' 선정은 저를 포함한 2명이서 수동으로 했습니다. 100% 올바른 요약이라고 가정할 수는 없습니다. 학습이나 실험을 한다면, dev용 데이터셋 정도의 역할만 할 수 있습니다.

### 데이터 구조 예시

`summaries`가 `sentences` 중 요약에 해당하는 문장의 index입니다. 이걸 정답셋으로 사용하시면 됩니다.

`length`는 문장 갯수를 뜻합니다. `slug`는 그냥 `title`을 [python-slugify][1]로 돌린 결과입니다.

	{
		'title': "기사 제목",
		'source': "http://출처.출처",
		'slug': "can-be-used-as-unique-id",
		'length': 23,
		'summaries': [0, 1, 4, 7],
		'sentences': [
			"문장1",
			"문장2",
			...
		]
	}
		
[1]: https://github.com/un33k/python-slugify
