# Character attack in depth

If you are already read **How to add new weapon item**, In that part you will see about **WeaponData** which contains **Action Id**, **Animation Duration** and **Launch Duration** that you may doubt how it working.

* * *

About **Action Id** we use it to determine which animation will play when attacking, you should set it relates to condition in **CharacterAnimator** which located at  BattleIO/Demo/Animations

![](../images/1FIMrlNyczPJf4aYf6AFCdg.png)

You can open it to add new Animation for this example I will show how I adding **Spear** attack animation

![](../images/1wu9kA91vXOl-rUZh-MOuhg.png)

When you opened CharacterAnimator you will see tab like this

Then select **Top** layer because all attack animation have been set on that layer

![](../images/16kqE2lOsM2Wv7T5yxwkODg.png)

Select Top layer, then you will see Attack sub-state machine

Double click on **Attack** sub-state machine you will see how transition work to play attack animation

You can click on arrow line to see condition to play animation

![](../images/12pVTeDe_PGqrEI1zL3n2Zg.png)

Select any arrow line

![](../images/1egdXQoxHbhmdrQAiqyuZ9w.png)

See conditions in Inspector

Then I will add new attack animation named **Atk-Spear**

Right click on space in Animator tab then select Create State -> Empty

![](../images/1YT4xbvUjHmQ8wR9hJ89DVQ.png)

Then select new created State set it name to **Atk-Spear** and set its animation clip (Caution: Attack animation clip should not be loop)

![](../images/12ZsB8ZxJw-gFY71Q4RkF9g.png)

Then make transition from **Any State** to **Atk-Spear** and set its conditions

![](../images/1otaJ2WAkLxtsif3LBrG0zg.png)

![](../images/1AdYPSs1fwH_FmS4DrHm0ww.png)

As above settings, I set **Can Transition To Self** as **False** because I don’t want it playing attack animation while last attack animation is not finish

Conditions **DoAction** is required to make it start playing attack animation it have been defined by codes (CharacterEntity.cs), **ActionID** equals to **2** to make condition to play this animation when equip weapon with its **Action Id** data equals to **2**

Then make transition from **Atk-Spear** to **Up** and select **NonAttack** state machine

![](../images/1G3fbHZkCdKEH4igJBlWNYQ.png)

Then set conditions for this transition to stop playing this animation when **DoAction** equals to **False**

![](../images/1s2RW3b-klFptH2VV4h-JkQ.png)

Then set **Action Id** in item data which you want to make it play this animation to **2**

![](../images/1vNpF4fUcILuGkiKOEo8zhg.png)

* * *

Next is about **Animation Duration** and **Launch Duration**

For **Animation Duration** setting we have to see duration of the animation it’s easy just see it in Animation Clip

![](../images/1hGDNaAef3Pc6Mbfc7XN5lQ.png)

Then we’re going to find which duration is the frame attack character should launch damage entity, I’d recommend you to create new scene (File ->New Scene)

Then drag any character model (BattleIO/Demo/Prefabs/CharacterModel) to the scene and then open **Animation** tab via menu Window -> Animation

Select the character then in **Animation** tab select **AttackSpear** clip

![](../images/1wvEOZycC6YQ45W3C5doy3g.png)

Then select frame which you want to launch damage entity

![](../images/1Sp5IFWnaCmK7BQR0-Gd8fA.png)

In this example selected frame is 10 of 18, then use **Animation Duration** with this to find **Launch Duration**

Let’s 10 is which percent of 18, it’s easy 10 / 18 \* 100 = 55, so it’s 55 %

Then use this percent to find **Launch Duration**, When **Animation Duration** equals to 0.79, 0.79 \* 55 / 100 = 0.4345, so this is amount of **Launch Duration**

If you want to increase speed for animation clip you have to change number of Samples then find **Animation Duration** and **Launch Duration** again

![](../images/1GDCnTCF6AgloWzMjeCvZmA.png)

The number of Samples