open https://club.jd.com/myJdcomments/saveCommentSuccess.action

input：

spec4 = document.getElementsByClassName("btn-spec4")

if (spec4.length > 1)
{
    spec4[0].click()
}



after page loaded， input：

start5 = document.getElementsByClassName("star star5")
var items = start5

for (var i = 0; i < items.length; i++)
{
    items[i].className = "star star5 active"
}

tags = document.getElementsByClassName("tag-item")

var items = tags
i = 0
cnt = 0
for (i = 0; i < items.length; i++)
{
	if (items[i].innerText.endsWith("携带") && items[i].innerText.length==2) items[i].click()
        if (!items[i].innerText.endsWith("携带") && cnt < 5) {
            items[i].click()
            cnt ++
	}
}

textareas = document.getElementsByTagName("textarea")

for (i = 0; i < textareas.length; i++) {
    if (textareas[i].placeholder.endsWith("商品是否给力？快分享你的购买心得吧~")) {
	try {
		textareas[textareas.length - 1].innerText = "好，非常好，不好的话我才不买的。"
	} catch (e) {
		textareas[textareas.length - 1].outerText = "好，非常好，不好的话我才不买的。"
	}
    }
}

submitBtn = document.getElementsByClassName("btn-submit")

submitBtn[0].click()
