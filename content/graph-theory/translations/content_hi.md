# रेखांकन और नेटवर्क 

## परिचय 

> id: intro-0
> section: introduction

 हर दिन हम अनगिनत कनेक्शन और नेटवर्क से घिरे रहते हैं: सड़क और रेल ट्रैक, फोन लाइन, इंटरनेट, इलेक्ट्रॉनिक सर्किट और यहां तक कि आणविक बांड। यहां तक कि दोस्तों और परिवारों के बीच _सामाजिक नेटवर्क_ भी हैं। क्या आप किसी अन्य उदाहरण के बारे में सोच सकते हैं? 

::: column(width=220 parent="padded-thin")

    x-img(src="images/network1.jpg" width=220 height=220 lightbox)

{.caption} सड़क और रेल नेटवर्क 

::: column(width=220)

    x-img(src="images/network6.jpg" width=220 height=220 lightbox)

{.caption} कंप्यूटर चिप्स 

::: column(width=220)

    x-img(src="images/network3.jpg" width=220 height=220 lightbox)

{.caption} पहुंचाने का तरीका 

::: column(width=220)

    x-img(src="images/network2.jpg" width=220 height=220 lightbox)

{.caption} यारियाँ 

::: column(width=220)

    x-img(src="images/network7.jpg" width=220 height=220 lightbox)

{.caption} तंत्रिका संबंध 

::: column(width=220)

    x-img(src="images/network4.jpg" width=220 height=220 lightbox)

{.caption} इंटरनेट 

:::

---
> id: intro

::: column.grow

 गणित में, इन सभी उदाहरणों को [__ग्राफ़ के__](gloss:graph) रूप में दर्शाया जा सकता है (किसी फ़ंक्शन के _ग्राफ़_ के साथ भ्रमित नहीं होना)। एक ग्राफ में कुछ _बिंदु_ होते हैं जिन्हें [[कोने]] कहा जाता [[है | हलकों | क्रॉसिंग]] , जिनमें से कुछ [[किनारों से]] जुड़े हुए हैं [[| सीमाओं | जोड़े]] । 

 __ग्राफ सिद्धांत__ रेखांकन और उनके गुणों का अध्ययन है। यह गणित के सबसे रोमांचक और दृश्य क्षेत्रों में से एक है, और इसमें अनगिनत महत्वपूर्ण अनुप्रयोग हैं। 

::: column(width=180)

    svg#graph0.graph.novertices.noedges(width=180 height=180)

:::

---
> id: intro-1

 हम हलकों और रेखाओं का उपयोग करके सरल रेखांकन के लेआउट को आकर्षित कर सकते हैं। कोने की स्थिति और किनारों की लंबाई अप्रासंगिक है - हम केवल इस बात की परवाह करते हैं _कि वे_ एक दूसरे से _कैसे जुड़े हैं_ । किनारे भी एक दूसरे को पार कर सकते हैं, और सीधे होने की जरूरत नहीं है। 

::: column(width=200)

    svg.graph(height=120 width=200 style="margin: 0 auto .8em")

{.caption} कुछ रेखांकन में, किनारे केवल एक ही रास्ते पर जाते हैं। इन्हें [__निर्देशित रेखांकन__](gloss:directed-graph) कहा जाता [__है__](gloss:directed-graph) । 

::: column(width=200)

    svg.graph(height=120 width=200 style="margin: 0 auto .8em")

{.caption} कुछ ग्राफ़ में कई समूहों के समूह होते हैं जो किनारों से एक दूसरे से जुड़े नहीं होते हैं। ये ग्राफ __काट दिया जाता है__ । 

::: column(width=200)

    svg.graph(height=120 width=200 style="margin: 0 auto .8em")

{.caption} अन्य रेखांकन में एक ही जोड़े के बीच कई कोने हो सकते हैं, या कोने जो खुद से जुड़े होते हैं (लूप)। 

:::

    // TODO maybe include examples of graphs with edges crossing, curved edges, etc.
    // could include an "is this a graph?" quiz

---
> id: intro-2

 हम वर्टिकल और किनारों में से कुछ को हटाकर एक मौजूदा ग्राफ से नए ग्राफ बना सकते हैं। परिणाम को [__सबग्राफ__](gloss:subgraph) कहा जाता है। यहाँ आप ग्राफ़ के कुछ और उदाहरण देख सकते हैं, जिसमें रंगीन किनारों और एक संभावित उपसमूह को इंगित करने वाले कोने हैं: 

::: column(width=212 parent="padded-thin")

    svg.graph(height=100 width=100 style='float: left; margin-right: 12px')
    svg.graph(height=100 width=100 style='float: left')

::: column(width=212)

    svg.graph(height=100 width=100 style='float: left; margin-right: 12px')
    svg.graph(height=100 width=100 style='float: left')

::: column(width=212)

    svg.graph(height=100 width=100 style='float: left; margin-right: 12px')
    svg.graph(height=100 width=100 style='float: left')

:::

---
> id: intro-3

 हम कहते हैं कि ग्राफ़ का [__क्रम__](gloss:graph-order) उसके द्वारा लंबित संख्याओं की संख्या है। एक शीर्ष की [__डिग्री__](gloss:graph-degree) किनारों की संख्या है जो उस शीर्ष पर मिलते हैं। 

::: column(width=130)

    svg.graph(height=120 width=120 style='margin: 0 auto .8em')

{.text-center} क्रम: [[५]] 

::: column(width=130)

    svg.graph(height=120 width=120 style='margin: 0 auto .8em')

{.text-center} क्रम: [[8]] 

::: column(width=130)

    svg.graph(height=120 width=120 style='margin: 0 auto .8em')

{.text-center} डिग्री: [[३]] 

::: column(width=130)

    svg.graph(height=120 width=120 style='margin: 0 auto .8em')

{.text-center} डिग्री: [[6]] 

:::

---
> id: intro-4

 रेखांकन जो एक ही लूप के वर्टिकल से मिलकर बने होते हैं उन्हें [__चक्र__](gloss:graph-cycle) कहते हैं। सभी चक्रों [[में किनारों और कोने की समान संख्या होती है | कोने से अधिक किनारों | कोने कोने से कम]] । 

    .row
      svg.graph(style='width: 120px; height: 120px;')
      svg.graph(style='width: 120px; height: 120px;')
      svg.graph(style='width: 120px; height: 120px;')

{.reveal(when="blank-0")} इन नई परिभाषाओं से लैस, आइए रेखांकन के कुछ आकर्षक गुणों और अनुप्रयोगों का पता लगाएं। 

---
> id: bridges-0
> title: The Bridges of Königsberg
> section: bridges

## कोनिग्सबर्ग का पुल 

::: column.grow

 ग्राफ़ और नेटवर्क के बारे में सोचने वाले पहले गणितज्ञों में से एक [लियोनहार्ड यूलर थे](bio:euler) । बाल्टिक सागर के पास कोनिग्सबर्ग शहर के बारे में यूलर को एक पुरानी समस्या से घेर लिया गया था। 

 प्रागेल को कोनिग्सबर्ग को चार अलग-अलग हिस्सों में विभाजित किया गया है, जो सात पुलों से जुड़े हैं। क्या शहर के चारों ओर घूमना संभव है, एक बार में सभी पुलों को पार करना - लेकिन एक बार से अधिक नहीं? (आप कहीं भी शुरू कर सकते हैं और खत्म कर सकते हैं, जरूरी नहीं कि एक ही जगह पर हो।) 

 इन मानचित्रों पर आरेखण करके एक मान्य मार्ग खोजने का प्रयास करें: 

::: column(width=250)

    img.shifted(src="images/konigsberg1.jpg" width=250 height=350)

:::

---
> id: bridges
> goals: bridge-0 bridge-1 bridge-2 bridge-3
> title: The Bridges of Königsberg

    x-tabbox.full-width
      .tab
        h3 Map 1#[span.check.incorrect(when="bridge-0")]
        x-solved
        include svg/bridges-1.svg
        button.btn Clear
        button.btn.right Skip
      .tab
        h3 Map 2#[span.check(when="bridge-1")]
        x-solved
        include svg/bridges-2.svg
        button.btn Clear
        button.btn.right Skip
      .tab
        h3 Map 3#[span.check(when="bridge-2")]
        x-solved
        include svg/bridges-3.svg
        button.btn Clear
        button.btn.right Skip
      .tab
        h3 Map 4 #[span.check.incorrect(when="bridge-3")]
        x-solved
        include svg/bridges-4.svg
        button.btn Clear
        button.btn.right Skip

---
> id: bridges-1

 कोनिग्सबर्ग के मामले में एक वैध मार्ग खोजना असंभव प्रतीत होता है, लेकिन कुछ अन्य शहर काम करते हैं। यूलर एक सरल नियम खोजने में कामयाब रहा, जो कि किसी भी शहर में लागू हो सकता है, बिना बहुत संभावनाएं आज़माने के लिए - ग्राफ सिद्धांत का उपयोग करके। 

::: column.grow

 सबसे पहले, हमें शहर के नक्शे को किनारों और कोने के साथ रेखांकन में बदलने की आवश्यकता है। प्रत्येक द्वीप या भूमि का क्षेत्र [[एक शीर्ष]] द्वारा दर्शाया गया [[है | एक किनारे | एक क्षेत्र]] और दो क्षेत्रों को जोड़ने वाला प्रत्येक पुल एक संबंधित [[किनारे]] द्वारा दर्शाया गया है [[| शिखर | गली]] । 

{.reveal(when="blank-0 blank-1")} अब "हर पुल को एक बार पार करते समय एक शहर का दौरा" की समस्या "हर किनारे को एक बार ठीक करने के दौरान एक निरंतर स्ट्रोक के साथ एक ग्राफ खींचना" की समस्या बन गई है। 

::: column(width=200)

    include svg/konigsberg.svg

:::

---
> id: bridges-2

 कागज पर, कुछ अलग रेखांकन के साथ आते हैं और फिर काम करने की कोशिश करते हैं कि किन लोगों को एक एकल, निरंतर स्ट्रोक के साथ खींचा जा सकता है। 

    // p Try drawing these graphs with one continuous stroke:
    // p.todo Interactive coming soon…

---
> id: bridges-3
> goals: size prime eo

 बस शहर के नक्शे के लिए पहले की तरह, हम पाते हैं कि कुछ रेखांकन संभव है जबकि अन्य नहीं हैं। हमें यह समझने में मदद करने के लिए कि क्यों, हमें हर [डिग्री](gloss:graph-degree) को उसकी [डिग्री के](gloss:graph-degree) साथ लेबल करना चाहिए। फिर हम विभिन्न तरीकों से रंगों को रंग सकते हैं, और एक पैटर्न प्रकट करने का प्रयास कर सकते हैं: 

    figure
      x-select.var.tabs(:bind="colour")
        div(value="val") Value
        div(value="size") Size
        div(value="prime") Prime Numbers
        div(value="eo") Even and Odd
      .box
        p.no-voice(style="margin: 0"): strong These graphs are possible:
        include svg/vertex-orders-1.svg
        p.no-voice(style="margin: 1em 0 0"): strong These graphs are not possible:
        include svg/vertex-orders-2.svg

---
> id: bridges-4

 ग्राफ़ के लिए इन नंबरों की तुलना करना जो संभव हैं और जो संभव नहीं हैं, ऐसा लगता है कि एक ग्राफ खींचा जा सकता है अगर इसमें [[दो से अधिक "विषम" कोने नहीं हैं | केवल "भी" कोने हैं | 4 से बड़े एक आदेश के साथ कोई कोने नहीं है | विषम संख्या में कोने हैं | आदेश 3 का कोई कोने नहीं है]] । इस स्थिति को समझाया जा सकता है यदि हम ग्राफ में केवल एक शीर्ष को देखें: 

    x-slideshow
      .stage(slot="stage"): include svg/konigsberg-proof.svg
      .legend(slot="legend") Here you can see a single, magnified vertex in a graph.
      .legend(slot="legend") If we draw the graph, we will eventually have an edge leading towards this vertex, and then another one leading away. This makes two edges meeting at the vertex.
      .legend(slot="legend") Maybe the vertex is a crossing rather than a corner. In that case there will be another edge leading towards the vertex, and another edge leading away. Now we have four edges.
      .legend(slot="legend") And in some graphs, there may even be a third pair of edges leading towards and away from the vertex. Now there are six edges.
      .legend(slot="legend") Notice that, either way, there always is an even number of edges meeting at the vertex.
      .legend(slot="legend") The only two exceptions are the vertices where the path starts, and where it ends – these two may have an odd number of edges. If the start and end point are the same, all vertices in the graph are even.

---
> id: bridges-5

::: column.grow(parent="right")

 यदि आप कोनिग्सबर्ग के मानचित्र पर वापस स्क्रॉल करते हैं, तो आप पाएंगे कि विषम पुलों की संख्या के साथ दो से अधिक द्वीप हैं। इसलिए एक मार्ग जो हर पुल को एक बार पार करता है वह वास्तव में असंभव है - और यही लियोनार्ड यूलर ने खोजा था। 

 यूलर की खोज वास्तविक जीवन में विशेष रूप से उपयोगी नहीं लग सकती है, लेकिन रेखांकन कई अन्य भौगोलिक समस्याओं की नींव पर हैं, जैसे कि दो स्थानों के बीच निर्देशन। हम बाद में इनमें से अधिक अनुप्रयोगों की खोज करेंगे। 

::: column(width=240)

    x-img(lightbox width=240 height=260 src="images/prague.jpg")

:::

---
> id: handshakes-1
> section: handshakes

## हैंडशेक और डेटिंग 

::: column.grow

 आपको अपने दोस्तों के साथ एक शानदार जन्मदिन की पार्टी में आमंत्रित किया गया है। अपने आप को और मेजबान को शामिल करते हुए, वहाँ हैं ${hnd}{hnd|5|3,15,1} लोग उपस्थित 

 शाम को, जैसे ही मेहमान जाने के लिए तैयार होते हैं, हर कोई हर किसी के साथ हाथ मिलाता है। कुल कितने हैंडशेक हैं? 

 हम एक ग्राफ का उपयोग करके हैंडशेक का प्रतिनिधित्व कर सकते हैं: प्रत्येक व्यक्ति [[एक शीर्ष है | एक किनारे]] , और हर हाथ में [[एक धार है | एक शीर्ष]] । 

{.reveal(when='blank-0 blank-1')} अब ग्राफ में किनारों की संख्या गिनना आसान है। हम पाते हैं कि वहाँ के साथ ${hnd} लोग, वहाँ हैं ${hnd*(hnd-1)/2} हैंडशेक। 

::: column.s-hide(width=240)

    img.shifted(src="images/party.jpg" width=240 height152)
    svg.graph(style='width: 240px; height: 240px;')

:::

---
> id: handshakes-2

 बड़े ग्राफ़ में सभी किनारों को गिनने के बजाय, हम एक सरल सूत्र खोजने की कोशिश भी कर सकते हैं जो हमें _किसी भी_ संख्या में मेहमानों के लिए परिणाम बताता है। 

 हर एक ${n}{n|5|2,8,1} पार्टी के लोग हाथ मिलाते हैं ${n-1} अन्य। ये बनाता है ${n} × ${n-1} = ${n×(n-1)} कुल में हाथ मिलाना। _N_ लोगों के लिए, हैंडशेक की संख्या होगी [[`n×(n–1)`|`n×(n+1)`|`n^2`]] । 

    p.var(:html="handshakeTable(n)")
    x-gesture(target="#handshakes-2 x-var" slide="100,0")

---
> id: handshakes-2a

 दुर्भाग्य से यह जवाब काफी सही नहीं है। नोटिस कैसे <x-target to=".handshakes tr:first-child td:first-child, .handshakes tr:first-child td:nth-child(2)">शीर्ष पंक्ति पर पहले दो प्रविष्टियाँ</x-target> वास्तव में वही हैं, बस चारों ओर फ़्लिप। 

 वास्तव में, हमने हर हैंडशेक को [[दो बार]] गिना है [[| एक बार | तीन बार]] , _{span.reveal(when="blank-0")} दो लोगों में से प्रत्येक के लिए एक बार। इसका मतलब है कि सही संख्या के लिए हैंडशेक ${n}{n|5|2,25,1} मेहमान है `(var("n") × var("n-1"))/2 = var("n*(n-1)/2")` ।_ 

---
> id: handshakes-3

 हैंडशेक ग्राफ खास हैं क्योंकि हर वर्टेक्स हर दूसरे वर्टेक्स से जुड़ा होता है। इस संपत्ति वाले __रेखांकन__ को __पूर्ण रेखांकन__ कहा जाता है। 4 शीर्षकों के साथ पूरा ग्राफ अक्सर संक्षिप्त होता है `K_4` 5 सिरों के साथ पूर्ण ग्राफ के रूप में जाना जाता है `K_5` , और इसी तरह। 

 हमने अभी-अभी दिखाया है कि एक पूर्ण ग्राफ़ के साथ `n` कोने, `K_n` , है `(n × (n-1))/2` किनारों। 

    .row
      svg.graph(style="width: 90px; height: 90px")
      svg.graph(style="width: 90px; height: 90px")
      svg.graph(style="width: 90px; height: 90px")
      svg.graph(style="width: 90px; height: 90px")

---
> id: handshakes-4

    figure: img(src="images/flags.jpg" width=855 height=100)

 एक अलग दिन में, आपको एक स्पीड डेटिंग इवेंट के लिए आमंत्रित किया जाता है ${m}{m|5|2,8,1} लड़के और ${f}{f|4|2,8,1} लड़कियाँ। कई छोटी टेबल हैं और हर लड़का लड़कियों के साथ 5 मिनट बिताता है। कुल कितने "दिनांक" हैं? 

::: column.grow

 इस स्थिति में, संबंधित ग्राफ में दो अलग-अलग सेट होते हैं। प्रत्येक शीर्ष [[विपरीत]] में सभी कोने से जुड़ा हुआ है [[| अपने स्वयं के]] सेट, लेकिन [[अपने आप में]] कोई भी कोने [[नहीं है | विपरीत]] सेट। जिन ग्राफ़ों में यह लेआउट होता है, उन्हें __द्विदलीय ग्राफ़__ कहा जाता है। 

::: column(width=300)

    svg.graph(style="width: 300px; height: 140px;")

:::

{.reveal(when="blank-0 blank-1")} साइज़ _x_ और _y के_ दो सेट के साथ द्विदलीय ग्राफ को अक्सर लिखा जाता है `K_"x,y"` । यह है [[`x×y`|`x+y`|`2x–y`]] किनारों, _{span.reveal(when="blank-2")} जिसका अर्थ है कि उपरोक्त उदाहरण में हैं ${m} × ${f} = ${m×f} खजूर।_ 

---
> id: utilities
> goals: try-three-times
> section: planar-graphs

## प्लेनर रेखांकन 

::: column.grow

 यहां एक और पहेली है जो ग्राफ सिद्धांत से संबंधित है। 

 एक छोटे से गांव में तीन घर और तीन उपयोगिता संयंत्र हैं जो पानी, बिजली और गैस का उत्पादन करते हैं। हमें प्रत्येक पाठ्यक्रम को प्रत्येक उपयोगिता पौधों से जोड़ना है, लेकिन गांव के लेआउट के कारण, विभिन्न पाइपों और केबलों को पार करने की अनुमति नहीं है। 

::: column(width=300)

    x-img(width=300 height=200 src="images/power-plant.jpg")

:::

 नीचे दी गई सभी यूटिलिटी कंपनियों में से प्रत्येक को, आपकी किसी भी पंक्तियों को जोड़ने के बिना, घरों को जोड़ने की कोशिश करें: 

    .box.no-padding
      include svg/utilities.svg
      button.btn Clear

---
> id: utilities-1

 पहले की तरह ही कोनिग्सबर्ग पुल, आपको जल्दी पता चलता है कि यह समस्या भी असंभव है। ऐसा लगता है कि ओवरलैपिंग किनारों के बिना कुछ ग्राफ खींचे जा सकते हैं - इन्हें __प्लानर ग्राफ__ कहा जाता है - लेकिन अन्य नहीं कर सकते। 

::: column(width=200)

    svg.graph(width=200 height=200 style="margin-bottom: .4em")

{.text-center}`K_3` प्लानर है। 

::: column(width=200)

    svg.graph#planar-2(width=200 height=200 style="margin-bottom: .4em")

{.text-center}`K_4` [[प्लानर है | प्लानर नहीं है]] । 

::: column(width=200)

    svg.graph#planar-3(width=200 height=200 style="margin-bottom: .4em;")

{.text-center}`K_5` [[प्लानर नहीं है | प्लानर है]] । 

:::

---
> id: utilities-2

 [पूरा ग्राफ](gloss:complete-graph) `K_5` सबसे छोटा ग्राफ है जो प्लानेर नहीं है। कोई अन्य ग्राफ़ जिसमें सम्‍मिलित है `K_5` किसी तरह से सबग्राफ के रूप में भी प्लानर नहीं है। यह भी शामिल है `K_6` , `K_7` , और सभी बड़े पूर्ण रेखांकन। 

 तीन उपयोगिताओं पहेली में [ग्राफ द्विदलीय ग्राफ है](gloss:bipartite-graph) `K_"3,3"` । यह पता चला है कि किसी भी गैर-प्लानर ग्राफ में या तो एक होना चाहिए `K_5` या ए `K_"3,3"` (या इन दो रेखांकन का एक [उपखंड](gloss:subdivision) ) एक [उपसमूह](gloss:subdivision) के रूप में। इसे _कुराटोस्की की प्रमेय_ कहा जाता _है_ । 

    // TODO Add bio of Kazimierz Kuratowski

---
> id: planarity
> goals: planarity

::: .box.f-blue

#### planarity 

    x-solved
    svg#planarity(viewBox="0 0 720 360")

 यह एक प्लानर ग्राफ है, लेकिन ${n}{n|7|5,20,1} कोने को खुरच दिया गया है। कोने को फिर से व्यवस्थित करें ताकि किनारों में से कोई भी ओवरलैप न हो। 

    p.btn-row: button.btn New Random Graph
    // TODO Maybe mention that the restriction to straight line edges in the Planarity puzzle isn't
    // a restriction that matters (Fáry's Theorem).

:::

---
> id: euler

### यूलर का फॉर्मूला 

 सभी प्लेन ग्राफ उन विमानों को विभाजित करते हैं जिन्हें वे कई क्षेत्रों में खींचते हैं, जिन्हें __चेहरे__ कहा जाता __है__ । 

::: column(width=200)

    include svg/euler-2.svg

{.text-center} [[6]] लम्बवत  
[[5]] चेहरे  
[[10]] किनारों  
_{span.euler-sum} 11 वृतियाँ + चेहरे_ 

::: column(width=200)

    include svg/euler-1.svg

{.text-center} [[8]] लम्बवत  
[[7]] चेहरे  
[[14]] किनारों  
_{span.euler-sum} 15 वर्टिकल + फेस_ 

::: column(width=200)

    include svg/euler-3.svg

{.text-center} [[12]] चक्कर  
[[13]] चेहरे  
[[24]] किनारों  
_{span.euler-sum} 25 वर्टिस + फेस_ 

:::

---
> id: euler-1

 इन संख्याओं की तुलना करते समय, आप देखेंगे कि किनारों की संख्या हमेशा [[एक कम होती है | बड़ा |]] फलकों की संख्या के साथ साथ कोने की संख्या की तुलना में [[एक ही।]] दूसरे शब्दों में, _{.b.blue} एफ_ + _{.b.green} वी_ = _{.b.red} E_ + 1. इस परिणाम को __Euler का समीकरण__ कहा जाता __है__ और इसका नाम उसी [गणितज्ञ के](bio:euler) नाम पर रखा गया है जिसने कोनिग्सबर्ग ब्रिजेस समस्या को हल किया। 

 दुर्भाग्य से, अनंत रूप से कई ग्राफ हैं और हम यह देखने के लिए हर एक की जांच नहीं कर सकते हैं कि क्या यूलर का समीकरण काम करता है। इसके बजाय हम एक सरल [प्रमाण](gloss:proof) खोजने की कोशिश कर सकते हैं जो किसी भी ग्राफ के लिए काम करता है ... 

---
> id: euler-2

    x-slideshow
      .stage(slot="stage")
        svg(viewBox="0 0 640 200")
          line.link(style="stroke-width: 3px; display: none" x1=270 y1=30  x2=150 y2=100)
          line.link(style="stroke-width: 3px; display: none" x1=150 y1=100 x2=270 y2=170)
          line.link(style="stroke-width: 3px; display: none" x1=270 y1=170 x2=390 y2=100)
          line.link(style="stroke-width: 3px" x1="390" y1="100" x2="270" y2="30")
          circle.node(cx=270 cy=30  r=7)
          circle.node(cx=150 cy=100 r=7 style="display: none")
          circle.node(cx=270 cy=170 r=7 style="display: none")
          circle.node(cx=390 cy=100 r=7 style="display: none")
    
        .euler-table
          table.grid.table-small
            tr
              td: strong.blue.i F
              td: strong.green.i V
              td: strong.red.i E
            tr
              td.xf 0
              td.xv 1
              td.xe 0
          p.no-voice #[strong.blue.xf 0] + #[strong.green.xv 1] &nbsp;=&nbsp; #[strong.red.xe 0] + 1
    
      .legend(slot="legend") The simplest graph consists of a single vertex. We can easily check that Euler’s equation works.
      .legend(slot="legend") Let us add a new vertex to our graph. We also have to add an edge, and Euler’s equation still works.
      .legend(slot="legend") If we want to add a third vertex to the graph we have two possibilities. We could create a small triangle: this adds one vertex, one face and two edges, so Euler’s equation still works.
      .legend(slot="legend") Instead we could simply extend the line by one: this adds one vertex and one edge, and Euler’s equation works.
      .legend(slot="legend") Let’s keep going: if we now create a quadrilateral we add one vertex, two edges and one face. Euler’s equation still works.

---
> id: euler-3

 किसी भी (परिमित) ग्राफ का निर्माण एक शीर्ष के साथ शुरू करके और एक-एक करके अधिक शीर्ष जोड़कर किया जा सकता है। हमने दिखाया है कि, जो भी हम नए कोने जोड़ते हैं, यूलर का समीकरण मान्य है। इसलिए यह सभी ग्राफ के लिए मान्य है। 

 हमने जिस प्रक्रिया का उपयोग किया है उसे __गणितीय प्रेरण__ कहा जाता है। यह बहुत से मामलों में परिणाम साबित करने के लिए एक बहुत ही उपयोगी तकनीक है, बस सबसे सरल मामले से शुरू करके, और यह दिखाते हुए कि अधिक जटिल मामलों का निर्माण करते समय परिणाम हर कदम पर होता है। 

    .svg-block: include svg/dominoes.svg

---
> id: euler-4

 कई प्लानर रेखांकन बहुत [बहुकोणीय आकृति](gloss:polyhedron) का जाल, [बहुभुज](gloss:polygon) चेहरों के साथ तीन आयामी आकार के समान दिखाई। यदि हम पॉलीहेड्रा को लोचदार बैंड से बना मानते हैं, तो हम उन्हें सपाट होने तक कल्पना कर सकते हैं, जब तक कि वे फ्लैट नहीं हो जाते, प्लैनर ग्राफ: 

::: column(width=300)

    img.img-sequence(src="images/cube/cube0.png" width=300 height=300)
    x-slider(steps=31)

::: column(width=300)

    img.img-sequence(src="images/dodecahedron/dodeca0.png" width=300 height=300)
    x-slider(steps=31)

:::

---
> id: euler-5

 इसका अर्थ है कि हम यूलर के फार्मूले का उपयोग न केवल प्लानर ग्राफ के लिए, बल्कि सभी पॉलीहेड्रा के लिए भी कर सकते हैं - एक छोटे अंतर के साथ। पॉलीहेड्रा को रेखांकन में बदलने पर, चेहरों में से एक गायब हो जाता है: पॉलीहेड्रा का सबसे ऊपरी चेहरा "बाहर" बन जाता है; रेखांकन के। 

 दूसरे शब्दों में, यदि आप की संख्या गिनते हैं __{.red} किनारों__ , __{.blue} चेहरे__ और __{.green}__ _किसी भी_ पॉलीहेड्रॉन के __कोने__ , आप पाएंगे _{.b.blue} एफ_ + _{.b.green} वी_ = _{.b.red} ई_ + [[२]] । 

::: column(width=200)

    x-video(width=200 height=200 src="images/icosahedron.mp4" hover loop)

{.caption} __विंशतिफलक__  
__{.blue} 20__ चेहरे  
__{.green} 12__ चक्कर  
__{.red} 30__ किनारों 

::: column(width=200)

    x-video(width=200 height=200 src="images/rhombi.mp4" hover loop)

{.caption} __Rhombicosidodecahedron__  
__{.blue} 62__ चेहरे  
__{.green} 60__ चक्कर  
__{.red} 120__ किनारों 

::: column(width=200)

    x-video(width=200 height=200 src="images/football.mp4" hover loop)

{.caption} __कटे हुए इकोसाहेड्रॉन__  
__{.blue} 32__ चेहरे (12 काले, 20 सफेद)  
__{.green} 60__ चक्कर  
__{.red} 90__ किनारों 

:::

---
> id: maps
> section: map-colouring

## नक्शा रंग 

::: column.grow

 हमने पहले से ही कुछ नक्शे के साथ ग्राफ सिद्धांत का उपयोग किया है। जैसे ही हम बाहर ज़ूम करते हैं, व्यक्तिगत सड़कें और पुल गायब हो जाते हैं और इसके बजाय हम पूरे देशों की रूपरेखा देखते हैं। 

 जब नक्शा रंगना - या किसी अन्य ड्राइंग में अलग-अलग क्षेत्रों से मिलकर - आसन्न देशों में समान रंग नहीं हो सकता है। हम भी संभव के रूप में कुछ अलग रंगों का उपयोग करना चाहते हैं। 

 कुछ सरल "नक्शे", एक शतरंज की बिसात की तरह, केवल दो रंगों (काले और सफेद) की आवश्यकता होती है, लेकिन अधिकांश जटिल नक्शों की अधिक आवश्यकता होती है। 

::: column(width=240 style="margin-top: -10px")

    x-img.shifted(src="images/globe.jpg" width=240 height=320)

:::

---
> id: maps-1
> goals: map-0 map-1 map-2 map-3
> title: Colouring Maps

 अमेरिकी राज्यों के नक्शे को रंगते समय, 50 रंग स्पष्ट रूप से पर्याप्त हैं, लेकिन बहुत कम आवश्यक हैं। नीचे दिए गए मानचित्रों को यथासंभव रंगों से रंगने का प्रयास करें: 

    .four-colour-icons
      for i in [1, 2, 3, 4, 5, 6, 7]
        .four-colour-icon(tabindex=0)
    
    x-tabbox.four-colours.full-width
      .tab
        h3 United States #[span.check(when="map-0")]
        x-solved
        .colour-count(style="margin-bottom: -32px") #[span 0] colours used
        include svg/colours-1.svg
        button.btn.clear Clear
        // Note that states or countries which only share a corner are allowed to have the same colour.
        // Alaska and Hawaii are isolated from all of the other states and can have any colour.
      .tab
        h3 South America #[span.check(when="map-1")]
        x-solved
        .colour-count #[span 0] colours used
        include svg/colours-2.svg
        button.btn.clear Clear
      .tab
        h3 Germany #[span.check(when="map-2")]
        x-solved
        .colour-count #[span 0] colours used
        include svg/colours-3.svg
        button.btn.clear Clear
      .tab
        h3 England #[span.check(when="map-3")]
        x-solved
        .colour-count #[span 0] colours used
        include svg/colours-4.svg
        button.btn.clear Clear

---
> id: maps-2
> title: The Four Colour Theorem

::: column.grow

 इन सभी मानचित्रों को केवल चार अलग-अलग रंगों के साथ रंगा जा सकता है, लेकिन यह कल्पना करना मुश्किल नहीं है कि अन्य, बहुत जटिल मानचित्रों को कई और रंगों की आवश्यकता हो सकती है। वास्तव में, कुछ मानचित्रों __को कम से कम__ चार रंगों की आवश्यकता होती है, जब भी वे चार देश होते हैं तो सभी एक दूसरे से जुड़े होते हैं। 

::: column(width=200)

    img(src="images/four-colours.png" width=200 height=120)

:::

 पहले की तरह, हम एक मानचित्र को देशों और सीमाओं के साथ एक प्लानर ग्राफ में बदल सकते हैं: हर देश [[एक शीर्ष]] बन जाता [[है | एक किनारे | एक चेहरा]] , और [[एक सीमा साझा करने वाले]] देश [[|]] एक किनारे से एक [[ही रंग]] जुड़ा हुआ है: 

    .svg-block: include svg/colour-graph.svg

{.reveal(when="blank-0 blank-1")} अब हम एक ग्राफ के कोने को रंग देना चाहते हैं, और दो कोने का एक अलग रंग होना चाहिए यदि वे एक किनारे से जुड़े हुए हैं। 

---
> id: maps-3

::: column(width=240 parent="right")

    x-img(lightbox width=240 height=320 src="images/england-counties.jpg")

::: column.grow

 1852 में, वनस्पति विज्ञान के छात्र [फ्रांसिस गुथरी](bio:guthrie) को इंग्लैंड में काउंटियों के मानचित्र को रंगना था। उन्होंने देखा कि चार रंग किसी भी मानचित्र के लिए पर्याप्त लग रहे थे, जो उन्होंने कोशिश की थी, लेकिन उन्हें ऐसा कोई प्रमाण नहीं मिला जो _सभी_ मानचित्रों के लिए काम करता हो। यह एक अत्यंत कठिन समस्या बन गई और इसे __चार रंग प्रमेय के__ रूप में जाना जाने लगा। 

 अगले 100 वर्षों के दौरान, कई गणितज्ञों ने चार रंग प्रमेय के लिए "सबूत" प्रकाशित किए, केवल बाद में पाए जाने वाली गलतियों के लिए। इन अमान्य सबूतों में से कुछ इतने ठोस थे कि त्रुटियों की खोज में 10 साल से अधिक का समय लग गया। 

 एक लंबे समय के लिए, गणितज्ञ यह साबित करने में असमर्थ थे कि चार रंग पर्याप्त हैं, या एक नक्शा खोजने के लिए जिसे चार से अधिक रंगों की आवश्यकता है। 

:::

---
> id: maps-4

 1976 तक चार रंग समस्या पर थोड़ी प्रगति की गई थी, जब [वोल्फगैंग होकेन](bio:haken) और [केनेथ अपेल](bio:appel) ने अंत में इसे हल करने के लिए एक कंप्यूटर का उपयोग किया था। उन्होंने 1936 के विशेष मामलों में असीम रूप से कई संभावित मानचित्रों को कम कर दिया, जो प्रत्येक कंप्यूटर द्वारा 1000 घंटे से अधिक समय के लिए जांचे गए थे। 

    x-parallax.full-width(background="images/ibm-360.jpg")

---
> id: maps-5

 चार रंग प्रमेय एक कंप्यूटर का उपयोग करके सिद्ध किया जाने वाला पहला प्रसिद्ध गणितीय प्रमेय है, ऐसा कुछ जो तब से बहुत अधिक सामान्य और कम विवादित हो गया है। तेज़ कंप्यूटर और अधिक कुशल एल्गोरिदम का मतलब है कि आज आप कुछ घंटों में लैपटॉप पर चार रंग प्रमेय साबित कर सकते हैं। 

    figure
      x-img(src="images/suffice.jpg" width=320 height=80 credit="http://www.math.illinois.edu/History/postmarks.pdf")
      p.caption Postmark for the Department of Mathematics at the University of<br/>Illinois Urbana-Champaign, where Haken and Appel worked.

---
> id: maps-6

::: column.grow

 चार रंग प्रमेय केवल एक समतल विमान या एक क्षेत्र पर नक्शों के लिए काम करते हैं, और जहाँ सभी देश एक ही क्षेत्र से मिलकर बने होते हैं। 

 हालांकि गणितज्ञों ने _साम्राज्यों के_ मानचित्रों पर भी ध्यान दिया है, जहां देशों में कई डिस्कनेक्ट किए गए घटक शामिल हो सकते हैं, और अलग-अलग आकार के ग्रहों पर, जैसे कि एक टोरस (डोनट आकार)। इन मामलों में आपको चार से अधिक रंगों की आवश्यकता हो सकती है और प्रमाण और भी कठिन हो जाते हैं। 

::: column(width=300)

    x-video(width=300 height=220 src="images/torus.mp4" hover loop)
    p.caption This map on a torus requires seven colours.

:::

---
> id: salesman
> section: travelling-salesman

## यात्रा विक्रेता समस्या 

::: column.grow(parent="right")

 आइए, एक बार और सोचें, नेटवर्क और मैप के बारे में। कल्पना कीजिए कि एक डिलीवरी सेवा पर जाना है ${tsn}{tsn|8|2,50,1} पार्सल वितरित करने के लिए विभिन्न शहर। हम इन शहरों को एक ग्राफ में कोने के रूप में सोच सकते हैं। यदि सभी शहर सड़कों से जुड़े हैं, तो यह एक [[पूरा ग्राफ है | चक्र | द्विदलीय ग्राफ]] , इसलिए हैं <mfrac><mrow>${tsn} × ( ${tsn} - (1)</mrow><mn>2</mn></mfrac> = ${tsn*(tsn-1)/2} कुल में किनारों। 

 डिलीवरी ट्रक को सभी शहरों का दौरा करना है, किसी भी क्रम में। कोनिग्सबर्ग पुलों की समस्या में हम उन रास्तों को ढूंढना चाहते थे जो _हर_ एक _किनारे पर_ एक साथ यात्रा करते हैं। अब हम उन रास्तों को ढूंढना चाहते हैं जो _हर शिखर पर_ एक ही बार आते हैं। इन रास्तों को __हैमिल्टनियन चक्र__ कहा जाता __है__ । 

::: column(width=260)

    x-img(src="images/truck.jpg" width=260 height=280)

:::

---
> id: salesman-1

 संपूर्ण रेखांकन में हैमिल्टनियन चक्रों की अनगिनत अलग-अलग संभावनाएँ हैं। वास्तव में, हम किसी भी शीर्ष को वर्टेक्स शुरू करने के रूप में चुन सकते हैं और फिर किसी भी क्रम में शेष शहरों में से कोई भी चुन सकते हैं: 

    .row
      .grow: p.todo Diagram coming soon…
      .grow: p.todo Diagram Coming Soon…

---
> id: salesman-2

 के साथ एक ग्राफ में ${tsn1}{tsn1|4|2,10,1} शहरों, हर हैमिल्टन चक्र में भी होना चाहिए ${tsn1} शहरों। अभी, 

    ul.var(:html="tsmString(tsn1)")

 इसका मतलब है कि, कुल मिलाकर, वहाँ हैं ${tsnPaths(tsn1)} संभव पथ। इस उत्पाद के लिए एक आशुलिपि है ${tsn1} ! या ${tsn1} __कारक__ । 

 आप कल्पना कर सकते हैं कि दो शहरों के बीच सीधे यात्रा करना संभव नहीं हो सकता है - बिना किसी दूसरे शहर से गुजरे। उस मामले में अब हमारे पास पूरा ग्राफ नहीं है, और हैमिल्टनियन चक्रों की संख्या का पता लगाना, अगर वे बिल्कुल मौजूद हैं, तो यह और अधिक कठिन हो जाता है। 

---
> id: salesman-3

::: column.grow(parent="right")

 अब तक हमने इस तथ्य को नजरअंदाज कर दिया है कि कुछ शहर दूसरों की तुलना में आगे हो सकते हैं। वास्तविक जीवन में, हालांकि, यह एक बहुत ही महत्वपूर्ण विचार है: हम केवल _कोई_ रास्ता नहीं खोजना चाहते हैं, लेकिन हम सबसे छोटा रास्ता खोजना चाहते हैं। इसे __ट्रैवलिंग सेल्समैन प्रॉब्लम__ कहा जाता है। इसे न केवल परिवहन और रसद में, बल्कि माइक्रोचिप्स पर ट्रांजिस्टर की स्थिति, तेजी से कंप्यूटर बनाने के लिए, या [डीएनए](gloss:dna) की संरचना का विश्लेषण करते समय हल करना होगा। 

 एक सरल तरीका यह होगा कि सभी संभव रास्तों को आज़माया जाए, प्रत्येक की लंबाई का पता लगाया जाए, और फिर सबसे छोटा रास्ता चुना जाए। हालाँकि हमने अभी-अभी भी, केवल साथ ही दिखाया है ${tsn2}{tsn2|10|2,20,1} शहर हैं ${tsn2} ! = ${factorial(tsn2)} संभव पथ। एक बार जब आपके पास सैकड़ों या हजारों कोने होते हैं, तो शक्तिशाली कंप्यूटर का उपयोग करते हुए सभी संभव पथों की कोशिश करना असंभव हो जाता है। 

::: column(width=220)

    x-img(lightbox src="images/microchip.jpg" width=210 height=365)

:::

---
> id: salesman-4
> goals: move

 दुर्भाग्य से यात्रा विक्रेता समस्या को हल करने के लिए अधिक कुशल एल्गोरिदम नहीं है। इसके बजाय, गणितज्ञों और कंप्यूटर वैज्ञानिकों ने विभिन्न एल्गोरिदम विकसित किए हैं जो _अच्छे_ समाधान _ढूंढते_ हैं, भले ही वे बहुत अच्छे न हों। ये एल्गोरिदम, जो केवल अनुमानित समाधान देते हैं, को __Heuristics__ कहा जाता है। 

 इस नक्शे पर शहरों को फिर से व्यवस्थित करने का प्रयास करें, और देखें कि उनके बीच का सबसे छोटा रास्ता कैसे बदलता है। आप उन्हें टैप करके शहरों को निकाल सकते हैं, और आप मानचित्र पर कहीं भी (8 तक) क्लिक करके शहरों को जोड़ सकते हैं: 

    figure: .tsm
      svg(width=760 height=480 viewBox="0 0 760 480")

---
> id: salesman-5

::: column.grow

 __लालची एल्गोरिथ्म__ (या निकटतम पड़ोसी एल्गोरिथ्म) बहुत सरल है: आप एक यादृच्छिक शहर में शुरू करते हैं और लगातार उस निकटतम शहर में जाते हैं जिसे आपने पहले कभी नहीं देखा है। एक बार जब आप सभी शहरों का दौरा कर लेते हैं, तो आप रुक जाते हैं। 

::: column(width=300)

{.todo} एनीमेशन जल्द ही आ रहा है ... 

:::

 आप दिखा सकते हैं कि औसतन, लालची एल्गोरिथ्म का उपयोग करते हुए पाए जाने वाले मार्ग सबसे कम संभव पथ से 25% लंबे हैं। 

---
> id: salesman-6

::: column.grow

 __2-ऑप्ट एल्गोरिथ्म__ एक यादृच्छिक संभव पथ के साथ शुरू होता है। फिर आप बार-बार दो किनारों को उठाते हैं और उन्हें चारों ओर स्वैप करते हैं यदि यह मार्ग की लंबाई कम कर देगा। जब आप किनारों की किसी भी जोड़ी को अदला-बदली करके लंबाई को कम नहीं कर सकते, तो आप रुक जाते हैं। 

::: column(width=300)

{.todo} एनीमेशन जल्द ही आ रहा है ... 

:::

---
> id: ants

 यह पता चला है कि, कंप्यूटरों के अस्तित्व में आने से बहुत पहले, प्रकृति ने विभिन्न स्थानों के बीच इष्टतम रास्तों को खोजने के लिए एक चतुर तरीका खोजा था: एंटी कॉलोनियों में। 

    x-parallax.full-width(background="images/ants.jpg")

 चींटियाँ अपने घोंसले और संभव खाद्य स्रोतों के बीच सबसे कम संभव मार्गों को खोजना चाहती हैं। वे रसायनों के माध्यम से एक दूसरे के साथ संवाद कर सकते हैं जो वे अपने निशान के साथ छोड़ देते हैं, और जो अन्य चींटियों का पालन कर सकते हैं। 

---
> id: ants-1

::: column.grow

 * चींटी कॉलोनी कई स्काउट्स को भेजती है जो शुरू में यादृच्छिक दिशाओं में यात्रा करते हैं। एक बार जब वे भोजन पा लेते हैं, तो वे फेरोमोन के निशान को पीछे छोड़ते हैं। * अन्य चींटियाँ जब किसी एक को खोजती हैं, तो उसका पीछा करती हैं, जो उन्हें भोजन की ओर ले जाती हैं। अपनी वापसी यात्रा पर वे अधिक फेरोमोन जमा करते हैं, इस प्रकार निशान को मजबूत करते हैं। * समय के साथ, फेरोमोन वाष्पित हो जाता है। एक रास्ता लंबा है, चींटियों को इसके साथ यात्रा करने में अधिक समय लगता है, और इसलिए फेरोमोन को वाष्पित होने में अधिक समय लगता है। दूसरी ओर, छोटे रास्ते, अधिक तेजी से प्रबलित हो सकते हैं, इसलिए उनकी ताकत तेजी से बढ़ जाती है। 

::: column(width=240)

{.todo} जल्द ही आ रहा है आरेख ... 

:::

---
> id: ants-2

::: column(width=220 parent="right")

    x-img(style="margin-top: 5px" src="images/ant.jpg" width=220 height=220)

::: column.grow

 चींटी कॉलोनी सिस्टम (एसीएस) एल्गोरिदम कई "आभासी" चींटियों का उपयोग करते हुए, कंप्यूटर पर इस व्यवहार को दोहराने की कोशिश करते हैं। वे यात्रा सेल्समैन समस्या के लिए बहुत अच्छे समाधान पा सकते हैं। 

 एसीएस एल्गोरिदम की एक विशेष रूप से उपयोगी संपत्ति यह है कि वे लगातार चल सकते हैं और ग्राफ में बदलाव के लिए वास्तविक समय में अनुकूलित कर सकते हैं। ये परिवर्तन कार दुर्घटनाओं और सड़क नेटवर्क पर सड़क के बंद होने या कंप्यूटर नेटवर्क पर वेब सर्वर पर ट्रैफिक स्पाइक्स के कारण हो सकते हैं। 

:::

---
> id: ants-3

::: column(width=140)

    img(src="images/binary.jpg" width=140 height=320)

::: column.grow

 ट्रैवलिंग सेल्समैन की समस्या [एनपी-हार्ड है](gloss:np) , जिसका अर्थ है कि कंप्यूटर द्वारा हल किया जाना बहुत मुश्किल है (कम से कम बड़ी संख्या में शहरों के लिए)। 

 तेज़ और सटीक एल्गोरिदम खोजने से कंप्यूटर विज्ञान के क्षेत्र में गंभीर प्रभाव पड़ेगा: इसका मतलब होगा कि _सभी_ एनपी-हार्ड समस्याओं के लिए तेज़ एल्गोरिदम हैं। यह अधिकांश इंटरनेट सुरक्षा को बेकार कर देगा, जो इस तथ्य पर निर्भर करता है कि कुछ समस्याओं को कंप्यूटर के लिए बहुत मुश्किल माना जाता है। 

 ट्रैवलिंग सेल्समैन की समस्या को हल करने के लिए एक तेज़ एल्गोरिथम खोजने से गणित और कंप्यूटर विज्ञान में सबसे प्रसिद्ध खुली समस्याओं में से एक, __पी एनपी__ समस्या का समाधान होगा। यह सात [मिलेनियम पुरस्कार समस्याओं](gloss:millennium-prize) में से एक है, प्रत्येक $ 1m पुरस्कार ले रहा है। 

:::

---
> section: scheduling
> sectionStatus: dev

## शेड्यूलिंग समस्याएं 

{.todo} जल्द आ रहा है 

---
> id: applications
> section: applications

## हर दिन के जीवन में रेखांकन 

 हमने पिछले अध्यायों में ग्राफ सिद्धांत के कई अलग-अलग अनुप्रयोग देखे हैं, हालांकि उनमें से कुछ थोड़े से वंचित थे। हालांकि, यह पता चलता है कि रेखांकन रोजमर्रा की जिंदगी में कई वस्तुओं, अवधारणाओं और प्रक्रियाओं की नींव पर हैं। 

::: column.grow

 उदाहरण के लिए, इंटरनेट एक विशाल, आभासी ग्राफ है। प्रत्येक शीर्ष एक व्यक्तिगत वेबपेज है, और प्रत्येक किनारे का अर्थ है कि दो पृष्ठों के बीच एक हाइपरलिंक है। ध्यान दें कि लिंक केवल एक ही रास्ते पर चलते हैं, इसलिए यह ग्राफ़ [[निर्देशित]] होता [[है | बहु लाइन | conected]] , और यह ग्राफ _बहुत, बहुत बड़ा है_ । 

    // * "can be viewed as" instead of "is a vast, virtual graph". "Every
    // vertex represens an individual webpage and every edge a hyperlink
    // from one page to another".

 कुछ वेबसाइट्स, जैसे कि विकिपीडिया या फेसबुक, में बहुत सारी इनकमिंग लिंक होती हैं, जबकि कई छोटी वेबसाइटों में बहुत कम इनकमिंग लिंक हो सकते हैं। यह अंतर्निहित अवधारणा है जिसका उपयोग Google खोज परिणामों को क्रमबद्ध करने के लिए करता है। 

::: column(width=240)

    img(credit="© Various" src="images/websites.png" width=240 height=240)

:::

---
> id: applications-1

 अधिक आने वाले लिंक वाली वेबसाइटें उच्च गुणवत्ता वाली होती हैं और उन्हें खोज परिणामों में सबसे ऊपर दिखाया जाना चाहिए। उदाहरण के लिए, "लंदन" की खोज करते समय, लंदन में छोटी दुकानों, या लंदन में रहने वाले लोगों के ब्लॉग से पहले आधिकारिक पर्यटक सूचना स्थल दिखाए जाते हैं। ग्राफ थ्योरी, __पेज रैंक एल्गोरिथम के__ इस सरल विचार ने Google को अन्य शुरुआती खोज इंजनों की तुलना में काफी बेहतर बना दिया। 

---
> id: applications-2

 मानव जाति द्वारा बनाया गया इंटरनेट अब तक का सबसे बड़ा नेटवर्क है। यह चित्र इंटरनेट से जुड़े सभी सर्वरों का बहुत छोटा अनुपात दिखाता है: 

    x-parallax.full-width(background="images/internet.jpg")
      .credit © LyonLabs, LLC and Barrett Lyon, 2014

---
> id: applications-3

 वेबसाइट और हाइपरलिंक्स एक _वर्चुअल_ ग्राफ बनाते हैं, वहीं कंप्यूटर, सर्वर, राउटर, फोन लाइन और केबल का _भौतिक_ नेटवर्क भी है। 

::: column.grow(parent="right")

 हर बार जब आप एक फोन कॉल करते हैं या एक वेबसाइट को लोड करते हैं, तो नेटवर्क ऑपरेटरों को किसी भी व्यक्तिगत केबल या कनेक्शन की क्षमता से अधिक के बिना, प्रेषक और रिसीवर को जोड़ने का एक तरीका खोजना होगा। ग्राफ़ सिद्धांत और संभावना एक विश्वसनीय सेवा की गारंटी देना संभव बनाती है, उदाहरण के लिए जब एक विशेष कनेक्शन व्यस्त है, तो विविधताएं ढूंढकर। 

::: column(width=220)

    x-img(lightbox src="images/phone.jpg" width=220 height=166)

:::

---
> id: applications-4

 परिवहन और नेविगेशन में ग्राफ भी महत्वपूर्ण भूमिका निभाते हैं। सभी फ़्लाइट, ट्रेन और सबवे नेटवर्क ग्राफ़ बनाते हैं, जिनका उपयोग कुशल शेड्यूल बनाते समय किया जा सकता है। सबसे पहचानने योग्य रेखांकन में से एक लंदन भूमिगत मानचित्र है: 

    figure: x-img(lightbox src="images/tube-map.png" width=720 height=480 credit="© Transport for London")

---
> id: applications-5

::: column.grow

 सभी सड़कें और मोटरवे भी एक बड़ा नेटवर्क बनाते हैं, जिसका उपयोग Google मैप जैसी नेविगेशन सेवाओं द्वारा किया जाता है जब दो दिए गए बिंदुओं के बीच सबसे छोटा मार्ग होता है। 

::: column(width=60)

    x-img(credit="© Google" src="images/google-maps.jpg" width=70 height=70)

:::

::: column(width=280)

    x-img(lightbox src="images/congestion.jpg" width=280 height=170)

::: column.grow

 भविष्य में, __इंटेलिजेंट ट्रांसपोर्टेशन सिस्टम__ स्मार्टफ़ोन और सेल्फ-ड्राइविंग कारों से एकत्र किए गए स्थान डेटा का उपयोग करके कारों को अधिक कुशलता से रूट करके भीड़ और दुर्घटनाओं को कम करेगा। यह हर साल सड़क पर खोए लाखों घंटे बचा सकता है, प्रदूषण को काफी कम कर सकता है, और आपातकालीन सेवाओं को तेजी से यात्रा करने की अनुमति देता है। 

:::

---
> id: applications-6

 यह छवि पूरे उत्तरी यूरोप में वाणिज्यिक एयरलाइन उड़ानों के नेटवर्क को दिखाती है। 

    x-parallax.full-width(background="images/flights.jpg")

---
> id: applications-7

 विज्ञान, इंजीनियरिंग या रोजमर्रा की जिंदगी में अनगिनत अन्य रेखांकन हैं: 

::: column(width=200)

    x-img(lightbox src="images/molecules.jpg" width=200 height=200)

{.caption} __अणुओं__ और क्रिस्टल ग्रिड में परमाणुओं के बीच लिंक एक ग्राफ बनाते हैं। 

::: column(width=200)

    x-img(lightbox src="images/epidemic.jpg" width=200 height=200)

{.caption} एक नेटवर्क का उपयोग करके __बीमारियों__ और महामारियों के __प्रसार को__ मॉडलिंग किया जा सकता है। 

::: column(width=200)

    x-img(lightbox src="images/evolution.jpg" width=200 height=200)

{.caption} जीव विज्ञान में, प्रजातियों के पूर्वजों को दिखाने वाले __विकासवादी पेड़__ एक ग्राफ बनाते हैं। 

::: column(width=200)

    x-img(lightbox src="images/network6.jpg" width=200 height=200)

{.caption} __इलेक्ट्रिक सर्किट__ और कंप्यूटर चिप्स के विभिन्न घटक एक नेटवर्क बनाते हैं। 

::: column(width=200)

    x-img(lightbox src="images/letters.jpg" width=200 height=200)

{.caption} __भाषाओं__ की व्याकरणिक संरचना को ग्राफ़ का उपयोग करके मॉडल किया जा सकता है, उदाहरण के लिए अनुवाद एल्गोरिदम बनाने के लिए। 

::: column(width=200)

    x-img(lightbox src="images/finance.jpg" width=200 height=200)

{.caption} ग्राफ़ में __प्रायिकता__ , __गेम थ्योरी__ और __वित्तीय गणित__ में कई अनुप्रयोग हैं। 

:::

---
> id: social

### सामाजिक नेटवर्क 

 अंत में, हम ग्राफ़ के एक विशेष रूप से अच्छे उदाहरण के बारे में सोचते हैं जो रोजमर्रा की जिंदगी में मौजूद हैं: सोशल मीडिया। यहाँ, कोने [[लोगों का]] प्रतिनिधित्व करते [[हैं | दोस्त | नेटवर्क]] और किनारे दोस्ती, पसंद, सदस्यता या अनुयायियों का प्रतिनिधित्व करते हैं। 

 जब हम सोशल मीडिया ग्राफ खींचते हैं, तो हम आपसी दोस्तों के कुछ __समूहों__ को देख सकते हैं, जो एक ही स्कूल में गए होंगे या एक ही शहर में रह सकते हैं। हम लोगों की __केंद्रीयता__ का भी निर्धारण कर सकते हैं, जो इस बात पर निर्भर करता है कि एक शीर्ष कैसे जुड़ा हुआ है, और जो सोशल मीडिया पर किसी व्यक्ति की लोकप्रियता का मापक हो सकता है। 

    figure: x-img(lightbox src="images/social-network.png" width=720 height=500)

---
> id: social-1

::: column.grow

 2014 में, फेसबुक के 1.4 बिलियन सक्रिय उपयोगकर्ता थे और कुल 200 बिलियन से अधिक मित्रता थी। सभी फेसबुक उपयोगकर्ताओं में से आधे के 200 से अधिक दोस्त हैं, और चूंकि हमारे अधिकांश दोस्तों के समान मित्र हैं, इसलिए हम आसानी से _दोस्तों के_ हजारों _दोस्तों के_ दसियों हो सकते हैं। 

 एक रोमांचक सवाल अब होगा: यदि आप किसी भी दो यादृच्छिक फेसबुक उपयोगकर्ताओं को चुनते हैं, तो आपको एक से दूसरे तक पहुंचने के लिए कितने "मैत्री किनारों" की आवश्यकता होगी? उदाहरण के लिए, दोस्तों के बीच की दूरी [[1 है]] , दोस्तों के दोस्तों के बीच की दूरी [[2 है]] , और इसी तरह। 

::: column(width=200)

    x-img(src="images/facebook-like.png" width=200 height=200)

:::

---
> id: social-2

 2016 में, फेसबुक ने यह निर्धारित करने के लिए [एक अध्ययन](https://research.facebook.com/blog/three-and-a-half-degrees-of-separation/) किया कि इसके उपयोगकर्ता एक दूसरे से कैसे जुड़े हैं। उन्होंने पाया कि औसतन, आप 3.57 अन्य लोगों के माध्यम से फेसबुक पर _किसी और_ से जुड़े हुए हैं। और इसमें सेलिब्रिटी, राजनेता या यहां तक कि रॉयल्टी शामिल हैं! 

 दूसरे शब्दों में, यदि आप दुनिया भर में अरबों उपयोगकर्ताओं में से किसी एक को चुनते हैं, तो संभवतः उनके पास एक मित्र का मित्र होगा जो आपके किसी मित्र का मित्र जानता है। हम कहते हैं कि __अलगाव के__ 3.57 __डिग्री हैं__ । 

    figure
      x-img(lightbox src="images/facebook.jpg" width=720 height=360 credit="© Facebook")
      p.caption Geographic visualisation of all Facebook friendships in 2010.

---
> id: social-3

::: column(width=200)

    x-img(credit="© Metro-Goldwyn-Mayer" src="images/six-degrees.jpg" width=200 height=265 style="border: 1px solid #ccc")

::: column.grow

 1929 में, जब हंगरी के लेखक [फ्रिगेस कारिन्थी](bio:karinthy) ने पहली बार "पृथक्करण के छह डिग्री" के विचार का प्रस्ताव रखा, तो कोई इंटरनेट या सोशल मीडिया नहीं था, लेकिन दुनिया पहले से ही अधिक परस्पर जुड़ने लगी थी। 

 1967 में, [स्टेनली मिलग्राम](bio:milgram) ने एक पहला अनुभवजन्य प्रयोग किया, जिसमें नेब्रास्का और कैनसस में रहने वाले 296 प्रतिभागियों को बोस्टन, मैसाचुसेट्स में रहने वाले एक विशेष व्यक्ति को एक पत्र देने के लिए कहा गया था। उन सभी को चिट्ठी भेजने के लिए एक दोस्त चुनना था, जिसने फिर दूसरे दोस्त को चुना। हर कदम पर, पत्र बोस्टन के करीब चला गया। मिलग्राम ने पाया कि औसतन केवल 5.2 मध्यवर्ती मित्र थे - 5.2 डिग्री पृथक्करण। 

:::

 आज, हम में से हर एक अनगिनत अदृश्य रेखांकन का हिस्सा है, जो हमारी सामाजिक बातचीत, यात्रा, इंटरनेट और प्रौद्योगिकी, विज्ञान, और बहुत कुछ को रेखांकित करता है।