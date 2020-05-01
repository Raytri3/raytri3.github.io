---
author: Raymond_Gabler
layout: post
title: "Houseplant CTF 2020"
excerpt: "Writeups for various CTFs I solved during the 2020 Houseplant CTF (riceteacatpanda)."
categories: [Capture The Flag]
---

Houseplant CTF is a capture the flag made with the new RiceTeaCatPanda - I must say they win the "Best Name" for a CTF award. The only thing I didn't like, and it is minor, is the fact they gave the hints to challenges w/o requesting them.
> 
> This is the link: https://discordapp.com/invite/QRhHGJA


&nbsp;
&nbsp;
---

# Beginners
IMHO, more CTFs need to include a Beginners section, where less experienced players can learn. The 9 challenges in this category could all be solved via [Cyberchef](https://gchq.github.io/CyberChef/). If you're not familiar w/ CyberChef I recommend getting used it. 

## Beginner1
> When Bob and Jia were thrown into the world of cybersecurity, they didn't know anything- and thus were very overwhelmed. They're trying to make sure it doesn't happen to you.  
> Let's cover some bases first.  
> `cnRjcHt5b3VyZV92ZXJ5X3dlbGNvbWV9`

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner1.png)
&nbsp;
Alternatively you can do it straight from Bash.
{% highlight bash %}
echo cnRjcHt5b3VyZV92ZXJ5X3dlbGNvbWV9 | base64 -d; echo
rtcp{youre_very_welcome}
{% endhighlight %}

**Flag is `rtcp{youre_very_welcome}`.**

## Beginner2
> Bob wanted to let you guys know that "You might not be a complete failure."  
> Thanks, Bob.  
> `72 74 63 70 7b 62 6f 62 5f 79 6f 75 5f 73 75 63 6b 5f 61 74 5f 62 65 69 6e 67 5f 65 6e 63 6f 75 72 61 67 69 6e 67 7d`  
> Hint! Still covering bases here.

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner2.png)
&nbsp;

**Flag is `rtcp{bob_you_suck_at_being_encouraging}`.**

## Beginner3
> Fun fact: Jia didn't actually know what this was when they first started out. If you got this, you're already doing better than them ;-;  
> `162 164 143 160 173 163 165 145 137 155 145 137 151 137 144 151 144 156 164 137 153 156 157 167 137 167 150 141 164 137 157 143 164 141 154 137 167 141 163 137 157 153 141 171 77 41 175`  
>  Hint! wow, these bases are getting smaller

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner3.png)
&nbsp;

**Flag is `rtcp{sue_me_i_didnt_know_what_octal_was_okay?!}`.**

## Beginner4
> Caesar was stabbed 23 times by 60 perpetrators... sounds like a modern group project  
> egpc{lnyy_orggre_cnegvpvcngr}

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner4.png)
&nbsp;

**Flag is `rtcp{yall_better_participate}`.**

## Beginner5
> beep boop  
> -- .- -. -.-- ..--.- -... . . .--. ... ..--.- .- -. -.. ..--.- -... --- --- .--. ...  
> Remember to wrap the flag in the flag format rtcp{something}

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner5.png)
&nbsp;

**Flag is `rtcp{MANY_BEEPS_AND_BOOPS}`.**

## Beginner6
> i'm so tired...  
> 26 26 26 26 26 26 26 26 19 12 5 5 16 9 14 7 9 14 16 8 25 19 9 3 19  
> Remember to wrap the whole thing in the flag format rtcp{}

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner6.png)
&nbsp;

**Flag is `rtcp{zzzzzzzzsleepinginphysics}`.**

## Beginner7
> Don't go around bashing people.  
> igxk{fmovhh_gsvb_ziv_nvzm}

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner7.png)
&nbsp;

**Flag is `rtcp{unless_they_are_mean}`.**

## Beginner8
> You either mildly enjoy bacon, think it's a food of the gods, or are vegan/vegetarian.  
> 00110 01110 00100 00000 10011 00101 01110 01110 00011 00011 01110 01101 10011 10010 10011 00000 10001 10101 00100  
> Remember to wrap the flag in rtcp{}

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner8.png)
&nbsp;

**Flag is `rtcp{GOEATFOODDONTSTARVE}`.**

## Beginner9
> Hope you've been paying attention! :D  
> Remember to wrap the flag with rtcp{}
> This last challenge was basically using most of the above techniques from the first 8.

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/beginner9.png)
&nbsp;

**Flag is `rtcp{nineornone}`.**

# Crypto
A common site I use for crypto challenges is [dcode](wwww.dcode.fr/en); it's good one to bookmark.

## Sizzle
> Due to the COVID-19 outbreak, we ran all out of bacon, so we had to use up the old stuff instead. Sorry for any inconvenience caused...
>
> Dev: William  
> Hint! Wrap your flag with rtcp{}, use all lowercase, and separate words with underscores.
> Hint! Is this really what you think it is?

The attached `encoded.txt` file gives:

```
....- ..... ...-. .--.- .--.. ....- -..-- -..-. ..--. -.... .-... .-.-. .-.-. ..-.. ...-- ..... .--.. ...-- .-.-- .--.- -.... -...- .-... ..-.- .-... ..-.. ...--
```
As the name "Sizzle" implies this is a Bacon cipher. Before we decode the cipher, we need to convert the -'s and .'s to 1's and 0's (or A's and B's if you prefer). To do so we use the find/replace function.

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/sizzle.png)
&nbsp;

**Flag is `rtcp{bacon_but_grilled_and_morsified}`.**

## CH3COOH
> Owaczoe gl oa yjirmng fmeigghb bd tqrrbq nabr nlw heyvs pfxavatzf raog ktm vlvzhbx tyyocegguf.  
> Tbbretf gwiwpyezl ahbgybbf dbjr rh sveah cckqrlm opcmwp yvwq zr jbjnar.  
> Slinjem gfx opcmwp yvwq gl demwipcw pl ras sckarlmogghb bd xhuygcy mk ghetff zr opcmwp yvwq ztqgckwn.  
> Rasec tfr ktbl rrdrq ht iggstyk, rrnxbqggu bl lchpvs zymsegtzf.  
> Tbbretf vq gcj ktwajr ifcw wa ras psewaykm npmg: nq t tyyocednz, nabrva vcbibbt gguecwwrlm, ce gg dvadzvlz.  
> Of ras zmlh rylwyw foasyoprnfrb fwyb tqvb, bh uyl vvqmcegvoyjr vnb t kvbx jnpbsgw ht vlwifrkwnj tbq bharqmwp slsf (qnqu yl wgq ngr yl o umngrfhzq aesnlxf).  
> Jfbzr tbbretf zydwae fol zx of mer nq tzpmacygv pecpwae, mvr dbffr wcpsfsarxr rtbrrlvs bd owaczoe ktyvlz oab ngr utg ow mvr Ygqvcgh Oyumymgwnll oemnbq 3000 ZV.  
> Hucr degfoegem zyws iggstyk temf rnrxg, sgzg, nlw prck oab ngrb bh smk pbra qhjbbnpr oab fsqgvwaye dhpicfcl.  
> Heyvsf my wg yegb ftjr zxsa dhiab bb Rerdggtb hpgg.  
> Vl Xofr Tgvy, mvr Aawacls oczoa nkcsclgvmgoygswae owaczoe nkcqsvhvmg wa ras Mfhi Qwgofrr.  
> Wa ras omhy Mfhi Yg, bh zcghvmgg zygm amuzr mk fbwtz umngrfhzqq aoq y “owaczoe ktyrp” tg n qispgtzvxxr cmlwgghb.  
> Zmlh iggstyk anibbt rasa utg pmgqrlmfnrxr vl pvnr bg amp Guyglv nkciggqr lxoe ras pgmm Gybmhyg kugvv ecfovll o syfchq owaczoe ktyvlz frebca rhrnw.  
> Foaw Vvvlxgr tbbretff ygr gfxwe slsf dhf psewaykm nlw arbbqvltz cskdbqxg jcks jpbhgcg rbug wa ras nekwpsehhptz zyginj Jwzgg Mnmlvh.  
> pmqc{tbbretf_bl_fm_sglv_nlw_qugig_cjxofc}  
> Hint! Short keys are never a good thing in cryptography.

The text was too long for Dcode so, I just copied the last portion. The key was TONY.

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/ch3cooh.png)
&nbsp;

**Flag is `rtcp{vinegar_on_my_fish_and_chips_please}`.**

## fences are cool unless they're taller than you
> They say life's a roller coaster, but to me, it's just jumping over fences.  
> tat_uiwirc{s_iaaotrc_ahn}pkdb_esg

It is a typical Rail Fence cipher - just used Cyberchef again :).

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/rail.png)
&nbsp;

**Flag is `rtcp{ask_tida_about_rice_washing}`.**

## Returning Stolen Archives
> So I was trying to return the stolen archives securely, but it seems that I had to return them one at a time, and now it seems the thieves stole them back! Can you help recover them once and for all? It seems they had to steal them one at a time...
>
>  Hint! Well you sure as hell ain't going to solve this one through factorization.

Notice that the Ciphertext is a series of letters? Good, we wont have to break anything we can just brute force it.
* `intercepted.txt`

```
n = 54749648884874001108038301329774150258791219273879249601123423751292261798269586163458351220727718910448330440812899799
e = 65537
ct = [52052531108833646741308670070505961165002560985048445381912028939564989677616205955826911335832917245744890104862186090,24922951057478302364724559167904980705887738247412638765127966502743153757232333552037075100099370197070290632101808468,31333127727137796897042309238173536507191002247724391776525004646835609286736822503824661004274731843794662964916495223,37689731986801363765434552977964842847326744893755747412237221863834417045591676371189948428149435230583786704331100191,10128169466676555996026197991703355150176544836970137898778443834308512822737963589912865084777642915684970180060271437,31333127727137796897042309238173536507191002247724391776525004646835609286736822503824661004274731843794662964916495223,32812400903438770915197382692214538476619741855721568752778494391450400789199013823710431516615200277044713539798778715,48025916179002039543667066543229077043664743885236966440148037177519549014220494347050632249422811334833955153322952673,52052531108833646741308670070505961165002560985048445381912028939564989677616205955826911335832917245744890104862186090,32361547617137901317806379693272240413733790836009458796321421127203474492226452174262060699920809988522470389903614273,4363489969092225528080759459787310678757906094535883427177575648271159671231893743333971538008898236171319923600913595,47547012183185969621160796219188218632479553350320144243910899620916340486530260137942078177950196822162601265598970316,32361547617137901317806379693272240413733790836009458796321421127203474492226452174262060699920809988522470389903614273,33230176060697422282963041481787429356625466151312645509735017885677065049255922834285581184333929676004385794200287512,32315367490632724156951918599011490591675821430702993102310587414983799536144448443422803347161835581835150218650491476,6693321814134847191589970230119476337298868688019145564978701711983917711748098646193404262988591606678067236821423683,32710099976003111674253316918478650203401654878438242131530874012644296546811017566357720665458366371664393857312271236,49634925172985572829440801211650861229901370508351528081966542823154634901317953867012392769315424444802884795745057309,50837960186490992399835102776517955354761635070927126755411572132063618791417763562399134862015458682285563340315570436]
```

* `solution.py`

{% highlight python %}
'#!/usr/bin/python3

'#Given N and E encrypt all characters and compare them to ciphertext
'#effiectively bruteforcing by encrypting all characters
'n=54749648884874001108038301329774150258791219273879249601123423751292261798269586163458351220727718910448330440812899799
e=65537
ct = [52052531108833646741308670070505961165002560985048445381912028939564989677616205955826911335832917245744890104862186090,24922951057478302364724559167904980705887738247412638765127966502743153757232333552037075100099370197070290632101808468,31333127727137796897042309238173536507191002247724391776525004646835609286736822503824661004274731843794662964916495223,37689731986801363765434552977964842847326744893755747412237221863834417045591676371189948428149435230583786704331100191,10128169466676555996026197991703355150176544836970137898778443834308512822737963589912865084777642915684970180060271437,31333127727137796897042309238173536507191002247724391776525004646835609286736822503824661004274731843794662964916495223,32812400903438770915197382692214538476619741855721568752778494391450400789199013823710431516615200277044713539798778715,48025916179002039543667066543229077043664743885236966440148037177519549014220494347050632249422811334833955153322952673,52052531108833646741308670070505961165002560985048445381912028939564989677616205955826911335832917245744890104862186090,32361547617137901317806379693272240413733790836009458796321421127203474492226452174262060699920809988522470389903614273,4363489969092225528080759459787310678757906094535883427177575648271159671231893743333971538008898236171319923600913595,47547012183185969621160796219188218632479553350320144243910899620916340486530260137942078177950196822162601265598970316,32361547617137901317806379693272240413733790836009458796321421127203474492226452174262060699920809988522470389903614273,33230176060697422282963041481787429356625466151312645509735017885677065049255922834285581184333929676004385794200287512,32315367490632724156951918599011490591675821430702993102310587414983799536144448443422803347161835581835150218650491476,6693321814134847191589970230119476337298868688019145564978701711983917711748098646193404262988591606678067236821423683,32710099976003111674253316918478650203401654878438242131530874012644296546811017566357720665458366371664393857312271236,49634925172985572829440801211650861229901370508351528081966542823154634901317953867012392769315424444802884795745057309,50837960186490992399835102776517955354761635070927126755411572132063618791417763562399134862015458682285563340315570436]
flag =""
for c in ct:
  #range 255 - all printable characters
  for i in range(255):
    #encrypts i and checks it w/ Ciphertext
    if pow(i,e,n) == c:
      #converts int to character and assigns it to flag
      flag += chr(i)
      break
  
print flag

{% endhighlight %}

**Flag is `rtcp{cH4r_bY_Ch@R!}`.**

## Rivest Shamir Adleman
> A while back I wrote a Python implementation of RSA, but Python's really slow at maths. Especially generating primes.
>
> Hint! There are two possible ways to get the flag ;-)

According to the hint there are multiple ways to solve this challenge. Looking thtough the files in chall.7z, I saw two avenues to try: 1. the low value of e 2. N and P are known. Note, I got P & Q from factordb and just used them. We could have used N and P to derive Q (n/p=q)

* `solution.py` 

{% highlight python %}
'#!/usr/bin/python3
from Crypto.Util.number import *
'#taken from secrets.txt.enc
ct="0x20ba6aee3bd1c1b751082bfcb667bad8b632504336f3994606594f4ab756f66e3a24f9782da3a07280aa67cd875e6e33f2c573abf7b7901e5cd428ab8ceb6738b13536fee35a90dac7c2175e41eea5977dfbaff6e68f5b1f6fa3673cba64923b02bff899e2535f7d09afecae6774260ce8be4867f45e63571a2055c645a03dd05d9dd596eec273e1ef4352d712deffc658745d17853cbe5c3bc138574703c994be5374e3ac73279f51f23ec7e55b25b6ab904e06562025c380ce4c4d5ddffc2d649fbd1421b82090d01f24c70254187f1f435e64d7b2bf8395915da3cfdd8680187566b6a51e48146b4a40f08aebdedca8a08557ea3dc5efc2c50377b5764a8c"
c=int(ct,16)
'# from public-key.json file
n = 5215102981058174620100754813213017625443626121109099133656454487932754235228856710661075956048331662593471061936196995326042367228980357932444477256496372200491821105922086202549125972429240337409176104237690646206864286971669895986447543904638596421264915837230690039800948447210554706127145724519079487023930504508462885777797916915752532472831523596571484341342780877665593787078959178539369282442522815729401991936772080063808078804309866694041173404657777517753433918322041736500126265865045225739241983004392226366771900174432875800986183772576663590650132115754645829772406067103501861326445534174181231077263
e = 5
'# Factorize Modulus using http://factordb.com/
p = 58754030774905986805754122995310081662217884210168479550129875193424398870745444673926050610118197084042202162420044553461740174815697964254570199939394803548997633592060223756279974260864378745120001533514186672141428133398599326104981445779780014073764199910798520251506148673445046102194538255507437319319
q = 88761620475672281797897005732643499821690688597370440945258776182910533850401433150065043871978311565287949564292158396906865512113015114468175188982916489347656271125993359554057983487741599275948833820107889167078943493772101668339096372868672343763810610724807588466294391846588859523658456534735572626377
'# Calculate totient function to find private key exponent
phi = (p-1)*(q-1)
d = inverse(e,phi)
flag = long_to_bytes(pow(c,d,n))
print flag

{% endhighlight %}

**Flag is `rtcp{f1xed_pr*me-0r_low_e?}`**

## Rainbow Vomit
> o.O What did YOU eat for lunch?!
>
> The flag is case insensitive.

We're given a file called `output.png`:

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/output.png)
&nbsp;

> Hint! Replace spaces in the flag with { or } depending on their respective places within the flag.  
> Hint! Hues of hex  
> Hint! This type of encoding was invented by Josh Cramer.  

Googling Josh Crammer and encoding we find that the picture is HexaHue. During my googlefu I found a decoder on [boxentriq](https://www.boxentriq.com/code-breaking/hexahue). I started decoding from the top and saw that was rabbit hole, so I moved to the last line and found the flag.

**Flag is `RTCP{SHOULD,FL5G4,B3,ST1CKY,OR,N0T}`.**

## Post-Homework Death
> My math teacher made me do this, so now I'm forcing you to do this too.
>
> Flag is all lowercase; replace spaces with underscores.
> Hint! When placing the string in the matrix, go up to down rather than left to right.  
> Hint! Google matrix multiplication properties if you're stuck.  

We're given one file:

```
Decoding matrix:

1.6  -1.4  1.8
2.2  -1.8  1.6
-1     1    -1


String:

37 36 -1 34 27 -7 160 237 56 58 110 44 66 93 22 143 210 49 11 33 22
```
It's just math, more specifically Matrix Mathmatics. Followng the hint, we had to enter the "string" from top down rather left to right. Seeing how the decoding method had three columns the other matrix has to be capped at 3 rows. I used [MatrixCalc](https://matrixcalc.org/en/#%7B%7B8/5,-%287/5%29,9/5%7D,%7B11/5,-%289/5%29,8/5%7D,%7B-1,1,-1%7D%7D%2A%7B%7B37,34,160,58,66,143,11%7D,%7B36,27,237,110,93,210,33%7D,%7B-1,-7,56,44,22,49,22%7D%7D). I then fed the results into CyberChef A1Z26 to get the final flag.

**Flag is `RTCP{go_do_your_homework}`.**

## 11
> I wrote a quick script, would you like to read it? - Daphne
>
>(doorbell rings)
>delphine: Jess, I heard you've been stressed, you should know I'm always ready to help!
>Jess: Did you make something? I'm hungry...
>Delphine: Of course! Fresh from the bakery, I wanted to give you something, after all, you do so much to help me all the time!
>Jess: Aww, thank you, Delphine! Wow, this bread smells good. How is the bakery?
>Delphine: Lots of customers and positive reviews, all thanks to the mention in rtcp!
>Jess: I am really glad it's going well! During the weekend, I will go see you guys. You know how much I really love your amazing black forest cakes.
>Delphine: Well, you know that you can get a free slice anytime you want.
>(doorbell rings again)
>Jess: Oh, that must be Vihan, we're discussing some important details for rtcp.
>Delphine: sounds good, I need to get back to the bakery!
>Jess: Thank you for the bread! <3

>Dev: Delphine
 >Hint! I was eleven when I finished A Series of Unfortunate Events.
 Hint! Flag is in format: rtcp{} format add _ (underscores) in place of spaces.
 Hint! Character names count too

Did some gooling on Series of Unfortunate Events and crypto and found that it is every 11th word between the "rings/knocks". Technically, from what I read it is the first word and then every 11th word and the names didn't count. I had to PM the dev, because my flag was putting in the first word.

**Flag is `rtcp{I'm_hungry_give_me_bread_and_I_will_love_you`.**


# Misc
## Spilled Milk
> oh no! i'm so clumsy, i spilled my glass of milk! can you please help me clean up?

A little hint always use stegsolve and check exif data for all pictures. We can see the flag using stegsolve.

&nbsp;
![]({{ site.baseurl }}/img/rtcp_ctf/spilledmilk.png)
&nbsp;

Flag is `rtcp{Th4nk$_f0r_h3LP1nG!`.

## Zip-a-Dee-Doo-Dah
> I zipped the file a bit too many times it seems... and I may have added passwords to some of the zip files... eh, they should be pretty common passwords right?

This is another multi-zip/zip crack challenge. Having seen this on a few CTFs I wrote a bash script a while ago that unzips, cracks passwds, and base64 decodes ascii (I believe it was Mitre 2019 that had base64 encoded zips). I will share the file on my gihub. Once it got through all 1800+ files we finally got the flag.

**Flag is `rtcp{z1pPeD_4_c0uPl3_t00_M4Ny_t1m3s_a1b8c687}`.**

# OSInt
## The Drummer who Gave all his Daughters the Same Name
> What is the value stored in the first registry key created by the virus Anna Kournikova?

Simple GoogleFu.

**Flag is `Worm made with Vbswg 1.50b`.**

## What a Sight to See!
> What Google Search Operator can I use to find results from a single website?

More GoogleFu..

**Flag is `site:`**

# Reverse Engineering
They had some real ez (literally) reversing challenges. I can do the basic ones but not the overly complex ones...yet.

## EZ
> I made a password system, bet you can't get the flag
Dev: William
Hint! Just a series of nice and relatively simple Python reverse engineering!

>We are given, a pass0.py file as seen below.

{% highlight python %}
print("rtcp{tH1s_i5_4_d3c0Y_fL4g_s0_DoNt_sUbm1T_1t!}")

'##they will never suspect a thing if i hide it here :)
'##print("rtcp{tH1s_i5_4_r3aL_fL4g_s0_Do_sUbm1T_1t!}")

{% endhighlight %}

**Flag is `rtcp{tH1s_i5_4_r3aL_fL4g_s0_Do_sUbm1T_1t!}`.**

## PZ
> I made a password system, bet you can't get the flag
Dev: William
Hint! Just a series of nice and relatively simple Python reverse engineering!

>We are given, a pass1.py file snippet below.

{% highlight python %}
def catcheckpass():
  userinput = input("pwease enter youwr password... uwu~ nya!!: ")
  if userinput == "rtcp{iT5_s1mPlY_1n_tH3_C0d3}":
      return True


{% endhighlight %}

**Flag is `rtcp{iT5_s1mPlY_1n_tH3_C0d3}`.**

# Lemon
> Fine. I made it a bit more secure by not just leaving it directly in the code.

Dev: William
 pass2.py  737e9ec98282f6831084dfe0b2eef879


{% highlight python %}
def catcheckpass():
 '' userinput = input("pwease enter youwr password... uwu~ nya!!: ")
   if userinput[0:4] == "rtcp":
        if userinput[10:13] == "tHi":
            if userinput[22:25] == "cuR":
                if userinput[4:7] == "{y3":
                    if userinput[16:19] == "1nT":
                        if userinput[7:10] == "4H_":
                            if userinput[13:16] == "S_a":
                                if userinput[19:22] == "_sE":
                                    if userinput [25:27] == "3}":
                                        return True

{% endhighlight %}

> Just reconstruct the flag from 0-25
**Flag is `rtcp{y34h_tHiS_a1nT_sEcuR3}`.**

