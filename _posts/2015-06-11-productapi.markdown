---
layout: nav
title:  "Product and Banner Ads API"
---

<h6>API for Product and Banner Ad serving</h6>


The API responses are modified to return the HTML response. Iframe tags are used to call these APIs from the webpage.

<strong>Resource URL:</strong>

http://test.snapdeal.com/pub/getAd?pub_id/impressionid/similar_ads/inv/category/adspaceId/pagetype/rs

<h6>Resource Information:</h6>

<strong>Response Format :</strong> JSON

<strong>Method:</strong> GET

<strong>Authentication:</strong> Optional

<h6>Input Parameters</h6>

<table class="table">
<th>Parameter Name</th>
<th>Details</th>
<th>Required</th>

<tr>
<td>pubid</td>
<td>Unique ID for the Publisher. For Snapdeal Inventory the default value is 1</td>
<td>Yes</td>
</tr>

<tr>
<td>js</td>
<td>Its a boolean Value that specifies whether JS tag is present</td>
<td>Optional</td>
</tr>

<tr>
<td>inv</td>
<td>This parameter denotes the type of inventory(App,msite or Website)</td>
<td>Optional</td>
</tr>

<tr>
<td>site id</td>
<td>Denotes the website from which the Ad request came(By default 101)</td>
<td>Optional</td>
</tr>

<tr>
<td>adspace id</td>
<td>Unique Id for the adspace/adslot in a particular page</td>
<td>Yes</td>
</tr>

<tr>
<td>impression id</td>
<td>Unique Id for the request</td>
<td>Yes</td>
</tr>

<tr>
<td>rs</td>
<td>Denotes the response type(HTML/JSON)</td>
<td>Optional</td>
</tr>

<tr>
<td>Category</td>
<td>The category type from which the request originated (Mobile/Fashion/Books)</td>
<td>Optional</td>
</tr>

<tr>
<td>Pagetype</td>
<td>The category type from which the request originated (Home/PDP/Thankyou)</td>
<td>Optional</td>
</tr>

<tr>
<td>similar ads</td>
<td>Its a boolean value that tells the system whether to return a similar ad or not</td>
<td>Required</td>
</tr>




</table>

 	 	 

<strong>Sample Request</strong>

GET

 http://52.5.245.198:9009/pub/getAd?pubId=1&js=true&siteId=101&impressionId=hello&similar_ads=false&inv=site&category=MOBI
 LES&adspaceId=1006&pagetype=category&rs=html

 
<strong>Sample Response</strong>


	<style>.sa_pa_style {position:relative;border:1px solid #ffffff;border-radius:2px;padding:2px;text-decoration:none;} .sa_pa_style:hover{border
	#fb8928;text-decoration:none;}.sa_pa_rating{background-image:url( http://sa.sdlcdn.com/adtech/images/icons/gridstars_sprite.png );backgroun
	no-repeat;height:10px;width:58px;padding-right:5px;margin-top:5px;float:left;} a:hover{text-decoration: none;}</style>
	<div style='width:166px;padding:10px 5px;float:left'>
	<div class='sa_pa_style'>
	<a href='52.5.295.198/rtb/clickTracker/1/531/hello?cb=1563280649&auid=${AUCTION_ID}' target='_self'>
	<div style='align:center;margin-bottom:5px;'>
	<img border='0' style='width:166px;height:194px;' src='http://sdstg.s3.amazonaws.com/imgs/a/a/a/166x194/SDL066442468_1372927343_image1
	mg >
	</div>
	<div style='font-size: 12px;color: #212121;word-wrap: normal;font-family: robotoMedium;margin-bottom: 4px;height: 30px;text-overflow: ellipsi
	-webkit-box;-webkit-line-clamp: 2;line-height: 15px;-webkit-box-orient: vertical;overflow: hidden;margin-top: 5px;max-height: 35px;'>
	Samsung Galaxy_WTTS7
	</div>
	<div style='position:static;margin-top:6px;'>
	<div style='font-size:16px;font-family:robotoMedium;color:#212121;text-decoration:none;font-weight:normal;'>Rs 32225 </div>
	<div style='font-size:13px;color:#565656;line-height:15pt;text-align:left;font-weight:normal;display:block;margin-top:0px;'>
	<div class='sa_pa_rating' style='background-position: 0px - 0 px;'></div>
	<div style='float:left;'>(0)</div>
	</div>
	<div style='clear:both'></div>
	<div
	style='color:#9e9e9e;font-size:12px;text-overflow:ellipsis;white-space:nowrap;overflow:hidden;line-height:20px;font-family:robotoRegular;disp
	156px !important;-webkit-box-orient:vertical;'>Sold by ST AANALYTICSIQ CONSULTING SERVICES PVT LTD </div>
	</div>
	<img border='0' width='1' height='1' src='52.5.295.198/rtb/impressionPixel/1/531/hello?cb=1706151826&vid=0&auid=${AUCTION_ID}' style='posi
	opacity: 0;width: 1px;height: 1px;'></img>
	</a>
	</div>
	</div>



<strong>Requests to the above APIs will result in one of 3 possible return codes:</strong> 

<table class="table">
<tr>
	<td>404 – BAD REQUEST</td>
	<td>Returned if there is a parameter mismatch in terms of format.</td>
</tr>
<tr>
	<td>500 – SERVER EXCEPTION</td>
	<td>Returned in case of exceptions on the server. For example, a connections failure, etc.</td>
</tr>
<tr>
	<td>200 – OK</td>
	<td>Returned if the request was processed properly. </td>
</tr>


</table>