---
layout: post
title:  "Unity - Rotate object towards target"
date:   2018-03-1
desc: "Rotate object towards a target"
keywords: "unity, quaternion, rotate, euler, rotatetowards"
categories: [Unity,C#]
tags: [Unity,C#]
icon: icon-csharp
---

A quick Unity-C# snippet for rotating an object to point towards a target

<?prettify?>
<pre class="prettyprint">
<h5 style="font-weight: 200">
Vector2 dir = tareget.transform.position - transform.position;
transform.rotation = Quaternion.Euler(0, 0, Mathf.Atan2(dir.y, dir.x)*Mathf.Rad2Deg - 90); // may not need 90 deg offset here;
</h5>
</pre>
---
