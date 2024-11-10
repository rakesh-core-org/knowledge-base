---
title: AboutMe
---

{{< blocks/cover title="Rakesh Technology Stack" image_anchor="top" height="full" >}}
<!-- <a class="btn btn-lg btn-primary me-3 mb-4" href="/docs/">
  Learn More <i class="fas fa-arrow-alt-circle-right ms-2"></i>
</a>
<a class="btn btn-lg btn-secondary me-3 mb-4" href="https://github.com/google/docsy-example">
  Download <i class="fab fa-github ms-2 "></i>
</a> -->
{{< blocks/link-down color="info" >}}

<p id="demo"></p>

<script>
var i = 0;
var txt = 'You work to live. I live to work 😍';
var speed = 100;

function typeWriter() {
  if (i < txt.length) {
    document.getElementById("demo").innerHTML += txt.charAt(i);
    i++;
    setTimeout(typeWriter, speed);
  }
}
typeWriter()
</script>

</body>
</html>


{{< /blocks/cover >}}


{{% blocks/lead color="primary" %}}

Technology keeps evolving, our primary focus is to adapt and go with the flow. 

      - Rakesh Nagarajan
{{% /blocks/lead %}}


{{% blocks/section color="dark" type="row" %}}
{{% blocks/feature icon="fa-lightbulb" title="wanna know more" %}}
<a href="https://rakeshnagarajanorg.github.io/" target="blank">See my online version</a>
{{% /blocks/feature %}}


{{% blocks/feature icon="fab fa-github" title="Open Source" %}}
Join with me in <a href="https://github.com/RakeshNagarajanOrg" target="blank" > Github</a>
{{% /blocks/feature %}}


{{% blocks/feature icon="fa-brands fa-linkedin" title="Reach out to me!" url="" %}}
I started to write learning materials in <a href="https://www.linkedin.com/in/rakesh-nagarajan/" target="blank" > LinkedIn</a>
{{% /blocks/feature %}}


{{% /blocks/section %}}


<!-- {{% blocks/section %}}
This is the second section
{.h1 .text-center}
{{% /blocks/section %}}


{{% blocks/section type="row" %}}

{{% blocks/feature icon="fab fa-app-store-ios" title="Download **from AppStore**" %}}
Get the Goldydocs app!
{{% /blocks/feature %}}

{{% blocks/feature icon="fab fa-github" title="Contributions welcome!"
    url="https://github.com/google/docsy-example" %}}
We do a [Pull Request](https://github.com/google/docsy-example/pulls)
contributions workflow on **GitHub**. New users are always welcome!
{{% /blocks/feature %}}

{{% blocks/feature icon="fab fa-twitter" title="Follow us on Twitter!"
    url="https://twitter.com/GoHugoIO" %}}
For announcement of latest features etc.
{{% /blocks/feature %}}

{{% /blocks/section %}} -->


<!-- {{% blocks/section %}}
This is the another section
{.h1 .text-center}
{{% /blocks/section %}} -->