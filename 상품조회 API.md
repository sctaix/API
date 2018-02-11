# 상품조회 API

# Request
<p>URL: http://api.petsdesign.co.kr/goods/{상품번호}[/{페이지번호}]</p>
<p>Require header: pd_key (해당키는 펫츠디자인 개발팀에 발급요청 하시기바랍니다. dev@petsdesign.co.kr)</p>

<p>* {상품번호}: 펫투비 상품번호</p>
<p>* 전체상품 조회시 {상품번호} = "all" ex) http://api.petsdesign.co.kr/goods/all[/{페이지번호}]</p>
<p>* 전체상품 조회시 페이징 처리가 되며, 한 페이지당 50개의 상품이 조회됩니다.</p>

# Response
<ul>
  <li>total: 조회된 상품수</li>
  <li>totalPageCnt: 전체 페이지수</li>
  <li>currentPage: 현재 페이지번호</li>
  <li>data: 상품정보(array)</li>
  <ul>
    <li>goodsNo: 상품번호</li>
    <li>goodsNm: 상품명</li>
    <li>categoryCode: 카테고리코드(SEPERATOR "|")</li>
    <li>categoryNm: 카테고리명(SEPERATOR "|")</li>
    <li>origin: 원산지</li>
    <li>maker: 제조사</li>
    <li>brand: 브렌드</li>
    <li>goodsPrice: 상품판매가(파트너사의 매입가)</li>
    <li>suggestionSalesPrice: 제안 판매가</li>
    <li>goodsDetail: 상품상세정보</li>
    <li>goodsImage: 상품이미지</li>
    <li>goodsStock: 상품재고수</li>
    <li>runout: 품절여부</li>
    <li>open: 진열여부</li>
    <li>EAD: 재입고일</li>
    <li>inPackageEA: 패키지 입수량</li>
  </ul>
  
</ul>

# Code sample
<blockquote>
	<p>cURL</p>
</blockquote>
<pre>
	<code>
		curl -X GET
		http://api.petsdesign.co.kr/goods/{상품번호} OR all[/{페이지번호}]
		-H 'cache-control: no-cache'
		-H 'pd_key: {발급받은 API key}'
	</code>
</pre>
