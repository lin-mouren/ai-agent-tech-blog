---
title: "사이클론 예측의 새로운 돌파구를 이끈 AI 모델"
vendor: google
source_url: https://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/
published_at: 2026-08-06T18:00:04.296Z
crawled_at: 2026-08-07T02:00:42.988Z
word_count: 1238
reading_time_minutes: 7
tags: [gemini, infrastructure, research]
---

# 사이클론 예측의 새로운 돌파구를 이끈 AI 모델

2026년 8월 6일

\|

읽는데 10 분 소요

- [x.com](https://twitter.com/intent/tweet?text=%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8%20%40google&url=https://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/)
- [페이스북](https://www.facebook.com/sharer/sharer.php?caption=%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8&u=https://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/)
- [링크드인](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/&title=%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8)
- [이메일](mailto:?subject=%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8&body=%EA%B5%AC%EA%B8%80%EC%BD%94%EB%A6%AC%EC%95%84%20%EB%B8%94%EB%A1%9C%EA%B7%B8%EC%97%90%EC%84%9C%20%EA%B2%8C%EC%8B%9C%EA%B8%80%20%EB%B3%B4%EA%B8%B0%0A%0A%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8%0A%0A%EA%B5%AC%EA%B8%80%EC%9D%B4%20%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%20%EC%A0%95%ED%99%95%EB%8F%84%EB%A5%BC%20%EB%86%92%EC%97%AC%20%ED%95%98%EB%A3%A8%20%EB%8D%94%20%EB%B9%A0%EB%A5%B8%20%EA%B2%BD%EB%B3%B4%20%EB%B0%9C%EB%A0%B9%EC%9D%84%20%EA%B0%80%EB%8A%A5%ED%95%98%EA%B2%8C%20%ED%95%98%EB%8A%94%20AI%20%EB%AA%A8%EB%8D%B8%20%27%EC%9B%A8%EB%8D%94%EB%84%A5%EC%8A%A4%ED%8A%B8%27%EB%A5%BC%20%EC%98%A4%ED%94%88%EC%86%8C%EC%8A%A4%EB%A1%9C%20%EA%B3%B5%EA%B0%9C%ED%95%A9%EB%8B%88%EB%8B%A4.%0A%0Ahttps://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/)
- 링크복사


구글이 사이클론 예측 정확도를 높여 하루 더 빠른 경보 발령을 가능하게 하는 AI 모델 '웨더넥스트'를 오픈소스로 공개합니다.


* * *

The WeatherNext team

Share


- [x.com](https://twitter.com/intent/tweet?text=%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8%20%40google&url=https://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/)
- [페이스북](https://www.facebook.com/sharer/sharer.php?caption=%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8&u=https://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/)
- [링크드인](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/&title=%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8)
- [이메일](mailto:?subject=%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8&body=%EA%B5%AC%EA%B8%80%EC%BD%94%EB%A6%AC%EC%95%84%20%EB%B8%94%EB%A1%9C%EA%B7%B8%EC%97%90%EC%84%9C%20%EA%B2%8C%EC%8B%9C%EA%B8%80%20%EB%B3%B4%EA%B8%B0%0A%0A%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%EC%9D%98%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EB%8F%8C%ED%8C%8C%EA%B5%AC%EB%A5%BC%20%EC%9D%B4%EB%81%88%20AI%20%EB%AA%A8%EB%8D%B8%0A%0A%EA%B5%AC%EA%B8%80%EC%9D%B4%20%EC%82%AC%EC%9D%B4%ED%81%B4%EB%A1%A0%20%EC%98%88%EC%B8%A1%20%EC%A0%95%ED%99%95%EB%8F%84%EB%A5%BC%20%EB%86%92%EC%97%AC%20%ED%95%98%EB%A3%A8%20%EB%8D%94%20%EB%B9%A0%EB%A5%B8%20%EA%B2%BD%EB%B3%B4%20%EB%B0%9C%EB%A0%B9%EC%9D%84%20%EA%B0%80%EB%8A%A5%ED%95%98%EA%B2%8C%20%ED%95%98%EB%8A%94%20AI%20%EB%AA%A8%EB%8D%B8%20%27%EC%9B%A8%EB%8D%94%EB%84%A5%EC%8A%A4%ED%8A%B8%27%EB%A5%BC%20%EC%98%A4%ED%94%88%EC%86%8C%EC%8A%A4%EB%A1%9C%20%EA%B3%B5%EA%B0%9C%ED%95%A9%EB%8B%88%EB%8B%A4.%0A%0Ahttps://blog.google/intl/ko-kr/company-news/technology/weathernext-2-cyclones-kr/)
- 링크복사


* * *



위험한 사이클론의 발달 양상을 예측하는 것은 단 1분 1초의 차이도 중요한, 오랫동안 이어져 온 난제입니다. 허리케인이나 태풍으로도 불리는 열대성 사이클론은 지구상에서 가장 파괴적인 기상 현상 중 하나로, 지난 50년 동안 전 세계에서 70만 명 이상의 사망자와 1조 4,000억 달러에 달하는 경제적 피해를 초래했습니다. 예보관들에게 정확한 경보를 적시에 발령하는 일은 언제나 시간과의 싸움입니다.

오늘 국제 학술지 ' [네이처(Nature)](https://www.nature.com/articles/s41586-026-10953-2)'에 게재된 논문을 통해, 구글은 AI 모델인 웨더넥스트(WeatherNext)가 사이클론의 이동 경로와 강도, 풍속 구조를 예측하는 데 있어 세계 최고 수준(state-of-the-art)의 정확도를 달성했다고 밝혔습니다. 웨더넥스트는 예보관들에게 평균적으로 하루 더 앞선 예측 정확도를 제공합니다. 즉, 기존 모델이 이틀 전까지 제공하던 수준의 예측 정확도를 웨더넥스트는 3일 전부터 미리 확보할 수 있게 된 것입니다. 이는 기존 기상학 분야에서 약 10년에 걸쳐 이뤄낸 기술적 진보와 맞먹는 커다란 도약입니다.

이번 연구는 구글 딥마인드(Google DeepMind)와 구글 리서치(Google Research)의 AI 연구원 및 엔지니어들이 [미국 국립허리케인센터](https://www.nhc.noaa.gov/)(National Hurricane Center, NHC), [미국 대기연구협동연구소](https://www.cira.colostate.edu/)(Cooperative Institute for Research in the Atmosphere, CIRA ), [영국 기상청](https://www.metoffice.gov.uk/)(UK Met Office)을 비롯한 전 세계 기상 기관의 예보 전문가들과 긴밀히 협력해 수행한 연구입니다.

이번 연구는 이미 실제 예보 현장에서도 성과를 내고 있습니다. 2025년 허리케인 시즌 동안, 웨더넥스트는 허리케인 '멜리사(Melissa)'의 급격한 세력 강화와 자메이카 상륙을 예측해 미국 국립허리케인센터가 [역사저인 사전 경보를 발령](https://deepmind.google/blog/how-weathernext-helped-the-national-hurricane-center-better-predict-hurricane-melissas-historic-landfall-in-jamaica/) 하는 데 기여했습니다. 이를 통해 현장 대응팀은 대피와 대비에 필요한 귀중한 골든타임을 확보할 수 있었습니다. 올해에도 구글은 주요 기상 기관들과 협력을 이어가며, 예보관들의 신속하고 정확한 의사결정을 지원하고자 사이클론마다 1,000개의 예측 시나리오를 제공하고 있습니다.

날씨는 우리 모두의 삶에 직접적인 영향을 미칩니다. 이러한 폭넓은 영향을 고려해 구글은 이번 허리케인 시즌에 활용된 '웨더넥스트 2(WeatherNext 2)'와 '웨더넥스트 사이클론즈(WeatherNext Cyclones)' 모델을 [오픈소스로 공개](https://github.com/google-deepmind/weathernext) 합니다. 구글은 이번 기술 공개를 통해 연구 커뮤니티가 이를 폭넓게 활용할 수 있도록 지원하고, AI가 더 회복력 있는 지역사회를 구축하는 데 기여하기를 기대합니다. 이는 지역 예보관이 [자연재해에 보다 효과적으로 대비](https://blog.google/innovation-and-ai/technology/research/helping-communities-prepare-for-natural-disasters/) 할 수 있도록 지원하는 것은 물론, 신재생에너지 발전량 예측 및 이상 기후 대비에 이르기까지 다방면에서 활용될 수 있습니다.

### **웨더넥스트의 기상 및 사이클론 예측 원리**



웨더넥스트 사이클론즈는 2024년 10월 허리케인 밀턴(Milton) 발생 당시의 전 지구 대기 상태 데이터를 바탕으로, 전 세계 기상 패턴과 정밀한 사이클론 이동 경로를 최대 15일 전까지 단계적으로 예측합니다. 또한 1,000개의 앙상블(ensemble) 모델을 구동해 열대성 폭풍부터 허리케인급 강풍에 이르는 지역별 재해 발생 확률 지도(probability map)를 생성합니다.

그동안 사이클론 예측은 서로 다른 두 가지 모델링 방식 간의 절충이 필요했습니다. 사이클론의 이동 경로, 즉 어디로 이동하는지는 거대한 전 지구 대기 흐름의 영향을 받기 때문에 상대적으로 해상도가 낮은 '전 지구 모델(global model)'이 적합했습니다. 반면 사이클론의 강도, 즉 얼마나 강해지는지는 중심부 주변에서 일어나는 미세하고 국지적인 열역학적 물리 과정에 의해 좌우되므로, 해상도가 높은 '특화 국소 모델(local model)'이 효과적이었습니다.

웨더넥스트는 전 지구 기상 예측과 사이클론 예측을 함께 개선함으로써 이러한 간극을 메웁니다. 단 하나의 AI 모델로 열대성 사이클론의 이동 경로와, 강도, 풍속 구조를 모두 세계 최고 수준의 정확도로 예측해 냅니다. 이러한 성과는 모델의 학습 방식과 아키텍처, 그리고 저해상도 입력 데이터를 처리하는 접근 방식을 독창적으로 결합한 결과입니다.



구글은 2023년부터 2024년까지 발생한 과거 사이클론 데이터를 바탕으로, 웨더넥스트 사이클론즈의 결정론적(deterministic) 및 확률론적(probabilistic) 예측 성능을 다른 최상위 기상 모델들과 비교 평가했습니다. 그 결과, 웨더넥스트 사이클론즈는 사이클론의 이동 경로, 강도, 풍속 구조 예측 전반에서 평균 하루(24시간) 이상 빠른 리드 타임(lead time) 우위를 보였습니다.

웨더넥스트는 전 지구 대기 역학 데이터와 전문가가 구축한 과거 사이클론 관측 데이터라는 두 가지 서로 다른 데이터 모달리티를 함께 학습했습니다. 약 20테라바이트에 달하는 전 지구 대기 데이터와 약 5,000건의 과거 폭풍 기록이 담긴 IBTrACS 데이터베이스를 엔드투엔드 방식으로 학습해, 복잡한 대기 패턴과 극한 기상 현상의 메커니즘을 모델링 할 수 있도록 설계되었습니다.



지난 수십 년간 기상학계는 위성 관측 기술과 예측 모델, 컴퓨팅 성능의 발전에 힘입어 3일 후의 사이클론 예측 정확도를 10년마다 약 하루꼴로 단축해 왔습니다. 웨더넥스트 사이클론즈는 단 한 번의 모델 공개만으로 10년 분량의 기술적 발전을 단번에 이뤄냈습니다.

웨더넥스트는 ['함수형 생성 네트워크(FGN: Functional Generative Networks)'](https://arxiv.org/pdf/2506.10772) 를 활용해 다양한 예측 결과로 구성된 앙상블을 효율적으로 생성하며, 날씨에 내재된 불확실성을 반영합니다. 이제 구글은 단 하나의 TPU(Tensor Processing Unit)만으로 1분 안에 15일 예보를 생성할 수 이으며, 이를 통해 예보관들은 피해 규모가 큰 극단적 위험의 발생 가능성을 보다 빠르게 평가할 수 있습니다. 지난해에는 기존 전 물리 모델과 마찬가지로 한 번에 50개의 시나리오를 예측했으나, 올해는 앙상블 규모를 1,000개로 대폭 확대해 2025년 허리케인 멜리사처럼 드물지만 파괴적인 세력 급강화 현상까지 놓치지 않고 포착할 수 있게 되었습니다.

지금까지는 사이클론의 강도를 정확히 예측하려면 매우 높은 공간 해상도가 필수적인 것으로 여겨졌습니다. 그러나 웨더넥스트 사이클론즈는 기존 모델보다 100배 낮은 해상도인 28x28km 데이터만으로도 뛰어난 예측 성능을 제공합니다. 이보다 더 낮은 111x111km 해상도로 동작하는 경량 모델 '웨더넥스트 2-미니(WeatherNext 2-mini)' 역시 우수한 성능을 보였습니다. 이러한 결과는 과학자들에게도 놀라운 발견이였으며, 이처럼 낮은 해상도에서도 어떻게 이토록 정확한 예측이 가능한지 밝혀내는 것 또한 향후 주요 연구 과제로 남아 있습니다. 구글은 글로벌 연구 커뮤니티와 손잡고 함께 그 원리를 파악해 나가기를 기대하고 있습니다.

### **웨더넥스트, 연구 커뮤니티를 위해 전면 공개**

구글은 네이처 논문 게재와 함께 모델의 소스 코드와 모델 가중치(model weights)를 [오픈소스](https://github.com/google-deepmind/weathernext) 로 공개합니다. 이를 통해 누구나 학술 연구는 물론 현장 기상 예보나 특정 지역에 특화된 정밀 예측 모델 개발 등 다양한 분야에서 자유롭게 활용할 수 있습니다. 구글은 이번 공개를 통해 글로벌 기상학계의 기술 발전을 앞당기고, 기상 기관과 연구자, 비영리 단체가 다양한 기상 현상을 더욱 정확히 예측해 생명과 사회 인프라를 보호하기 위한 중요한 의사결정을 내릴 수 있도록 지원하고자 합니다.

또한 구글은 유사한 두 가지 모델 라인업도 함께 공개합니다. 하나는 이번 허리케인 시즌 동안 운영된 '웨더넥스트 사이클론즈(WeatherNext Cyclones)'로, 관련 성과는 이번 논문에서 확인할 수 있습니다. 다른 하나는 지난해 10월 운영 환경에 적용한 후속 모델 '웨더넥스트 2'입니다. 또한 무료 공개 [코랩 노트북(Colab Notebook)](https://colab.research.google.com/github/google-deepmind/weathernext/blob/master/docs/weathernext2/wn2_demo.ipynb) 에서 단 하나의 TPU만으로 실행할 수 있는 경량 버전 '웨더넥스트 2-미니'도 함께 제공합니다.

최신 사이클론 예측은 최근 새롭게 개편된 ' [웨더 랩(Weather Lab)](https://deepmind.google.com/science/weatherlab/)' 웹사이트에서 바로 확인할 수 있습니다. 새 인터페이스를 적용한 웨더 랩은 사이클론 이동 경로뿐만 아니라 전 세계 기상 예측 정보까지 제공하도록 기능을 확대했습니다. 이제 기온, 강수량, 풍속 등 웨더넥스트의 다양한 예측 결과를 한눈에 직관적으로 살펴볼 수 있습니다. 웨더 랩과 웨더넥스트 모델은 모두 ' [구글 어스 AI(Google Earth AI)](https://ai.google/earth-ai/)' 프로젝트의 일부입니다.

### **AI 기반 기상 예측의 새로운 지평을 열다**

구글은 사이클론 예측에서 하루 이상의 추가 리드 타임을 확보하며, 기상학 분야에서 10년에 달하는 혁신을 단숨에 이뤄냈습니다. 앞으로 다가올 폭풍 시즌에 대비해 연구자와 기상 기관, 관련 전문가들이 오픈소스로 공개된 모델을 활용하고 웨더 랩의 예측 결과를 연구와 현장에 적극 활용하기를 기대합니다. 구글은 첨단 머신러닝 기술과 현장 전문가들의 전문성을 결합해, 생명을 지키고 기후 변화에 보다 효과적으로 대응할 수 있도록 지원하는 협력적 기상 예보 생태계를 만들어 가겠습니다.

- [**네이처 논문 읽어보기**](http://doi.org/10.1038/s41586-026-10953-2)
- [**코드 내려받기**](https://github.com/google-deepmind/weathernext)
- [**NHC 2025 검증 보고서 읽어보기**](https://www.nhc.noaa.gov/verification/pdfs/Verification_2025.pdf)

_참고: 공식 기상 예보 및 대피 경보는 각 지역 및 국가 기상청의 공식 발표를 확인하시기 바랍니다._

관련 키워드:

## 관련 게시글

[AI\\
**구글코리아 공식 인스타그램 오픈 소식을 전해드립니다** \\
\\
구글코리아의 새로운 소통 창구인 공식 인스타그램 채널(@googlekorea)이 정식 오픈했습니다!구글코리아 인스타그램에서는 구글의 최신 제품 소식은 물론, 일상을 더 편리하고 풍요롭게 만드는 다양한 활용 팁과 생생한 비하인드 스토리까지 다채로운 콘텐츠를 전해드릴 예정입니다.기술 이야기를 넘어 우리 일…](https://blog.google/intl/ko-kr/company-news/googlekorea-ig-open/)

[\\
\\
AI\\
**‘제미나이 로보틱스 ER 2(Gemini Robotics ER 2)’를 소개합니다**\\
\\
작성자\\
\\
\\
스티븐 한센(Steven Hansen)\\
\\
및 \\
펭 수(Peng Xu)](https://blog.google/intl/ko-kr/company-news/technology/gemini-robotics-er-2/)

[\\
\\
AI\\
**최신 음악 생성 모델 '리리아 3.5'로 더 감성 깊고 완성도가 높은 음악을 만들어 보세요**\\
\\
작성자\\
\\
\\
구글코리아 블로그 운영팀](https://blog.google/intl/ko-kr/company-news/technology/lyria-3-5-kr/)

[\\
\\
AI\\
**제미나이 로보틱스 2: 로봇에 전신 지능을 구현하다**\\
\\
작성자\\
\\
\\
캐롤리나 파라다(Carolina Parada)](https://blog.google/intl/ko-kr/company-news/technology/gemini-robotics-2/)

[\\
\\
Gemini\\
**\[요즘구글\] 내 잡무를 대신해 줄 '디지털 우렁각시'가 나타났다**\\
\\
작성자\\
\\
\\
구글코리아 블로그 운영팀](https://blog.google/intl/ko-kr/company-news/inside-google/gooseobang-ep17-gemini-spark/)

[\\
\\
AI\\
**구글이 ‘제미나이 3.6 플래시(Flash)’, ‘3.5 플래시-라이트(Flash-Lite)’, 그리고 ‘3.5 플래시 사이버(Flash Cyber)’를 소개합니다**\\
\\
작성자\\
\\
\\
툴시 도시(Tulsee Doshi)](https://blog.google/intl/ko-kr/company-news/technology/gemini-3-6-flash-3-5-flash-lite-3-5-flash-cyber/)