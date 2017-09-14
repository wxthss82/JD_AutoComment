# JD_AutoComment
自动化填写京东商品评论

github：https://github.com/wxthss82/JD_AutoComment/blob/master/README.md


open https://club.jd.com/myJdcomments/saveCommentSuccess.action  这是要待评价的商品列表

在 Chrome，开发者工具，Console 控制台中粘贴：

////////////////////////////////////////////////////////////////////////////////////////////

spec4 = document.getElementsByClassName("btn-spec4")

if (spec4.length > 1) { spec4[0].click() }

////////////////////////////////////////////////////////////////////////////////////////////

当新页面打开后，输入：

////////////////////////////////////////////////////////////////////////////////////////////

start5 = document.getElementsByClassName("star star5") var items = start5

for (var i = 0; i < items.length; i++) {    items[i].className = "star star5 active" }

tags = document.getElementsByClassName("tag-item")

var items = tags i = 0 cnt = 0 for (i = 0; i < items.length; i++) { if (items[i].innerText.endsWith("携带") && items[i].innerText.length==2) items[i].click() if (!items[i].innerText.endsWith("携带") && cnt < 5) { items[i].click() cnt ++ } }

textareas = document.getElementsByTagName("textarea")

for (i = 0; i < textareas.length; i++) { if (textareas[i].placeholder.endsWith("商品是否给力？快分享你的购买心得吧~")) { try { textareas[textareas.length - 1].innerText = "好，非常好，不好的话我才不买的。" } catch (e) { textareas[textareas.length - 1].outerText = "好，非常好，不好的话我才不买的。" } } }

submitBtn = document.getElementsByClassName("btn-submit")

submitBtn[0].click()

////////////////////////////////////////////////////////////////////////////////////////////

即可完成一次评价
