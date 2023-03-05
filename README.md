# JD_AutoComment
自动化填写京东商品评论


https://gist.github.com/cobola/4748c2d531b979d11042c8942134402b
请移步到该脚本，更方便和鲁棒，一键完成。


github：https://github.com/wxthss82/JD_AutoComment/blob/master/README.md


open https://club.jd.com/myJdcomments/saveCommentSuccess.action  这是要待评价的商品列表

在 Chrome，开发者工具，Console 控制台中粘贴：

/////////////////

spec4 = document.getElementsByClassName("btn-spec4");if (spec4.length > 1) { spec4[0].click() }

/////////////////

当新页面打开后，输入：

////////////

start5 = document.getElementsByClassName("star star5"); for (var i = 0; i < start5.length; i++) { start5[i].click()};textareas = document.getElementsByTagName("textarea");for (i = 0; i < textareas.length; i++) {{ try { textareas[textareas.length - 1].innerText = "好，非常好，不好的话我才不买的。" } catch (e) { textareas[textareas.length - 1].outerText = "好，非常好，不好的话我才不买的。" } } };submitBtn = document.getElementsByClassName("btn-submit");submitBtn[0].click();

/////////////

即可完成一次评价
