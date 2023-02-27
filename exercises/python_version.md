<!--- yes, this is an html page basically, but we want this to be embeded in our theme -->

<style>
#center {
    left: 50%;
    transform: translate(-50%, 0);
    position: absolute;
}
</style>

<div id="center">
    <iframe class="resizable" src="https://uflorida-my.sharepoint.com/personal/a_verma1_ufl_edu/_layouts/15/Doc.aspx?sourcedoc={b145d95d-7b40-4fe6-a5da-4225af19fb5b}&amp;action=embedview&amp;wdAr=1.7777777777777777" width="1024px" height="576px" frameborder="0">This is an embedded <a target="_blank" href="https://office.com">Microsoft Office</a> presentation, powered by <a target="_blank" href="https://office.com/webapps">Office</a>.</iframe>
</div>
<div class="resizable nowidth" style="width: 1px; height: 576px;"></div> 

<script>
function resizer() {
    const LENGTH_RATIO = 9.0/16.0;
    let width = screen.width;
    let height = 576;

    if (width < 1024) {
        height = Math.round(screen.width * LENGTH_RATIO);
    } else {
        width = 1024;
    }

    const collection = document.getElementsByClassName("resizable");
    for (let i = 0; i < collection.length; i++) {
        if (!collection[i].className.includes("nowidth")) {
            collection[i].style.width = width + "px";
        }
        collection[i].style.height = height + "px";
    }
}

window.addEventListener("resize", resizer);
resizer()
</script>