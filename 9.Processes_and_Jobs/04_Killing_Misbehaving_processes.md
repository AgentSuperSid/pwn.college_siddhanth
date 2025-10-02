# Killing Misbehaving Processes
in this challengewe are supposed to read and get the flag by killing a decoy program and running */challenge/run*

## My solve
**Flag:** `pwn.college{ccWu59dbUlxYvoR6InX7QyQWYmQ.0FNzMDOxwCO1kjNzEzW}`

- 
```bash
hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 12:36 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 12:36 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 12:36 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 12:36 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 12:36 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     137  0 12:36 ?        00:00:00 sleep 6h
root         141     138  0 12:36 ?        00:00:00 sleep 6h
hacker       142     139  0 12:36 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       144       0  0 12:36 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       150       0  0 12:36 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       156     144  0 12:36 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       159     150  0 12:36 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       174       0  0 12:36 pts/2    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       180     174  0 12:36 pts/2    00:00:00 /run/dojo/bin/bash --login
hacker       189     180  0 12:42 pts/2    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{4o1hbY1gouk-SUXuYu87nJTmXIseiX7klxwPQS5OXcPPxI6}
pwn.college{S.aL9FVQo4b.JkM8iIKkZctJJwQEEtN8uHFSertlaHirWyQ}
pwn.college{IIDhWgl4cejmp.oSuLQXq-XNxWpFG.7QNFXy10HFbNufs1L}
pwn.college{t0RaHpnGeqKbhj7JLKKSgLlwwVfSZ9SF14g.IJbzv8oBzW5}
pwn.college{Y3iluIT6q26zgdcUgYic5YYm-npYPpRfaakcnhq.we7HPm8}
pwn.college{khRm.BiKd1FGLzLvcHv6SFWDAQDViW-TGN.Zy1bMatJghFY}
pwn.college{VJVsygYYJgXERb5yZKlnFv8Aof31vIT7Qpx3CrZYYe9LsYl}
pwn.college{5y.FUpNqOHC61IdtPSeZtiJlp9KPrHr7SLrWBwXw7ktxtQC}
pwn.college{Q75xlS52WOPgyLJZl0XwWrDciEfDPGl2ELfmLwv7nVkLSq3}
pwn.college{4VWy.awGIFSJv7YHcURuXOjZxrq8naUUdROfEpaAsE5D8Xe}
pwn.college{nMNIVpSStklTlfyXm85K4QpnhJgH.8MtJ5nFsZ6UVKK6R8u}
pwn.college{N7USIAFbGqwDMIIyXELBf.M3Dg8EOIrBQbyo6kuQNvD0fKH}
pwn.college{iOqoikzrSl1YAbiMo3iEF9XloV90p7T2CA3uCRRB1D32EAK}
pwn.college{d.g-EljT39W0iPfLWME5aSS3ompGgDm4IxNpmNgQ7OCKlpz}
pwn.college{m9VUdpQZkY3PLme.GtWhTuclrn6Gfg-w6ZGbsDzdfdC4vAp}
pwn.college{TSwHfjpZYRaeV7JS9uDnTyNqLuYA5M21d4ZWsSDj3MfDxzV}
pwn.college{ySPrWVu.5HD-rS9XzBJAEfXwgX9gX2NhBpW5AzXdILyR0iA}
pwn.college{kZdCb7yLXh-DOjyZTOSRkSb9EwxvyIHM0crCjgFDzVkN2Yt}
pwn.college{NTMCwVb5WSS4KWZzEoJZmhWy86JsSuCWxx13Jn41wgdqR5I}
pwn.college{dhhgfoSt6-kPN7JKi5201dfHLqtG-IZrZACjjuK5qZSFJeI}
pwn.college{hlRZLJ.JJ.SKxl-eU5nVmqzMmeU3ulM3QCnSn8ssY.yuyts}
pwn.college{ERYZLjkSwX7PABq.0jaK0wtDrNejA77nkVwHpACxAMFqoBh}
pwn.college{900j1PpXJDYZlmsajqXnrHuZfGovFVqp0OcH5CPQEa0hqN7}
pwn.college{GjcAT2w-pxT4aKnhrwPqObjedlVf06Mi6inDD.6CV2lyoa8}
pwn.college{AfSeVSvxPehdfm6wEDv36ECAAOZbSwhAeomwJhHcfCDKkaU}
pwn.college{nFidt1bM0c1Ew82LJa2QGE9WUUtR3keK3-3zqY.1NkXTYze}
pwn.college{NwnGQdQdpff7MmMajBaXrbCL.eCyaUuuiTa3EgsOmtH1r4s}
pwn.college{qPBoWEuFTTst4T0CpYnGDTHYpKQFCzZwuPvMs2vx4kv-Cak}
pwn.college{IU6F0.5UVGxxOSY2qAXW7uzk3HhwhIPdZjM40CKn1IIhKA5}
pwn.college{jg4.qV4z8FmacBG3MC.fGA8InzcmCyXwHzzGej3k3Pr29cC}
pwn.college{q1fq7oUVmxPUpE69xpzxEXURWPFiWob1XM4xk3BF69XHxw5}
pwn.college{v54ZkCgiXV056zPJ7z8uC0YKjcouvJgW-58vZbuWqZF455T}
pwn.college{f3kHd2NiBdJqEUsuzB5q.FBlYmaQGh-p0mp931hIH4LmLyf}
pwn.college{YnAcdQoQT-havA.QZTjKbpIPRd951-dDDTj2llxjKLsJeMo}
pwn.college{RbdzDQ4IBs.FnA0xaQfKd5dWnG9dl2On2amuaTYij8kpYTM}
pwn.college{DJOZnZc6k.NcevSvTKnWGB34k6Djm.OR4He2yvGvpGFG39a}
pwn.college{lTZw4A2MDrsGnLHrhdN7n6rYK0G1J2SmemuMESpesMT1Rle}
pwn.college{plTtv1v9uRX.jwS4BS0rlKKw0mAtMzj5cKDrhW2mn-k8tLs}
pwn.college{HkLJwI1gU0dGo7M3nC8hks.6vMmBeKX2Nk1lWz8neFsJg7q}
pwn.college{Y9zf1YNHf-D5sFZhGOT-mPYbz9ZQXRdCPb3VW9FqhD1wQ.A}
pwn.college{ikbkNLA1jKV2ak-J0t5wHomlBOMrKPelQMASUC1Mo1g2RHS}
pwn.college{5bQ5fQpdTS3cCu4r1k1yPuUfJBQfb6ZsNI.IGG.l56IS01E}
pwn.college{MuJVw.qZ3mHU0Cu81-Vb5LACERcBtC.VdEPSTnToCJx1goL}
pwn.college{TDTlejEHzXBi6vmD1g.Ksp2yMtbJe.fF4xRPfj.dIHkbr2u}
pwn.college{aONKXE1CMoaYkokhFMZ8pf3KMQwpiT-f-Qdb77BsiECJLeO}
pwn.college{HDmvUHGD1lfr3uojI4Kd6y8vtbNRiuCM6H3hgO0K0BlSUh7}
pwn.college{62btF7iO3qsXoISPDs.gSu1Exc-rJf63thUTlzUxFQGbFrN}
pwn.college{un2LJ1YZMLBPAPGVeXl4K5iGk-N6dmNy.wL6YtlHpqN9X1Q}
pwn.college{BwhTzHYulTEcKEzOonIME7jG9qsGbPxLdFPaGyqL.n6I.n0}
pwn.college{bbVFUlwt8pUq.N6jebQRWvxfTMO9nXzZb4VeCken7rZdmkx}
pwn.college{lMrzebXaLaabQ.IL3sf03mthI7TWXKVoc0Cxxra18JPJltF}
pwn.college{JmajQsIrCC4Bgsqm1f8eFTNsy02L.pj5MVSZQhWp4C4CAZF}
pwn.college{85Ulpno6OC66RkHLHwTsIPjiawncmKp.28p2eJ8rdR51gck}
pwn.college{h0zENb8AzgsJKkShmKfUpYoBICaLTB7Gi.ZUlfNWN9djztC}
pwn.college{xAWuCHkIjkGva3N24nLPufUQs9Q1De8TUqoa4hZPXEYKwEP}
pwn.college{Uy-H3Lv8nDpJ7NE.0CmzYBiWreMwChth2BjsBu1nRSB4lUq}
pwn.college{aOODchnwQKU8XGpV9XjZpgvAiprQRVs1VWULMjnT7Lx.63-}
pwn.college{4-nNQHn.iiV4rKYrPOKnej20iUxWzYgiUQ4Bn7uOiuQiHUR}
pwn.college{yrMf1VVKOgLjRIx9inGwFQ5b2gdMfB4ey.ZcEV-J4mzAQQH}
pwn.college{BWv4yL8D4puFK4NQ3zZh5Q-.i8pNHNKcZwHrjqD-wpP2WN4}
pwn.college{vPNDQhC4twF0NjxrWUn8SKVQ8-WIfzQb8fhnFZenHpnsSdN}
pwn.college{Uf7axaEWfQFhazIfUePXzJlyW1sejawX6ApumEE1Rv5yhfo}
pwn.college{uVf2DTvLmQ25q5DSNoMPmCUcWmtP3NITEWu60P723pZjiYz}
pwn.college{3RE9ms6XbWR8ntfeZTjUer-VeeeVDGCtrpOjYT62UkXZAeF}
pwn.college{coR8104xDg33Swg3rYHKjW.gZIAo9MKJAl5sfFtcHT6-j4R}
pwn.college{4AkGDD06PQ1ZitsVZyI-B5xBhpHu2dV.MCh2Gm3oiOCtxCI}
pwn.college{F.NaU2GzOTUfs5OOOZHUSkMh-m9.v8zNd3UFuh99LAbyq0P}
pwn.college{Y.SugLqMJ1uzdRdltOVMkYakjDTnm3y1G86lbH2l5j8mRHv}
pwn.college{lNhZjrrCFOFtE19AAlfecOTMPJugSlLcRtBjlZokG8uFEs8}
pwn.college{we0iPqtu6VsFPwsYPsKFcC4-VBSN52M-0bjFHbwYd-Rj6zJ}
pwn.college{Q.5MdfoRGxGY2fG.ZKFitujzCiE-Q2e81jTkCc2kqPmQsFF}
pwn.college{nElPwTugl5zvJO46O0Q7tC7CWZbxIpTTMUkb2r9c8Os.tlG}
pwn.college{23ou6SsdPfGmWC0AE5r7SGJP2d7qrC-xfmx.Bw1Q0bi37oh}
pwn.college{dtq7yyyKXgkGtOHoSZMC3RvS27I0t0ulTqvcwVreiSJ.KsP}
pwn.college{5j7YiEGFwDjE6Olltjyq10nN3T9TOr26lUbs7s9pWWKtnI0}
pwn.college{DYKY1GCOm2yp647S6jO5XeuUq6ci7BulksefG-YfUYPv5Q-}
pwn.college{EClt3bfqoBR9uFSQ2OAdjCb-Ky2V2LTGb92aFGbB3Wov0Bn}
pwn.college{OqC5X9PstexH3yu8Pot-AIJfMhwvQo6YOjiLNg-pBw5E5lG}
pwn.college{AEp3ikXrbh.M8qNe4PvU84bN4U.BOqRnaO-zld4TEirc005}
pwn.college{1GFgn06Ll3D.cWyieXKXTM.uEUxb2JcV.5f3uUR3scfDOKF}
pwn.college{H7Ghfc3dUjqj8PThzKdQ9PgQTcax6pRH7KxJpZmi9HMEja3}
pwn.college{I1UftvVZALM3w7-yLzWT0zqXECktwbxWSHZjoPJ7MOUM1zn}
pwn.college{h3OHcGSnVSIrVV9GwhSUipgmJQ0B5pF1vCiAwGg3YxKcvrx}
pwn.college{gmfDTGHGTUzNi8mDcnHWxTi4o5ElP.yn9kiz7BMbJgbOEdu}
pwn.college{oPFQPbqp-rYNRS9uF7C9.sYkMnI8t.vo1twQ7Z0lR5EXvan}
pwn.college{0vt2mBu783ufLjZ4sjbYaUP.tEnH7HKiExTcP.4MuyvS31Q}
pwn.college{boMbtwnieuh173duhCN7rNW062jz0.soeVuyU.aF.H3l4J-}
pwn.college{9t2kOjjDCOUHLd6KFO-ghOQByfUQOmJAyoBn8TXTJRH6f5m}
pwn.college{pQ2a0FIfo5mAu-puOIEupuhrEuHesbglCT5aKUXYz8nJG3P}
pwn.college{83EobURQzcru9f-nDnLjQ5iDN1PQK95e.YhXG8RRz8Kmpbe}
pwn.college{VUSrG6V.0r1tqlCwV0HZBEjoaJjR7q5lw19MU53y8TbIa0N}
pwn.college{wBd5jqOM0eBSSa4KYlzcQ5cj5tql8t.n53mZ8FINMega73X}
pwn.college{lNKQjLCTrx.qukaqdElL3Aahcq7Z1GDpjtMOCvi-ItV-d1a}
pwn.college{vak.hc7MxupgTDTMqz8ae2FmETJE5OYJ6F4MEP2i.07Q-oO}
pwn.college{2J7gUNgoN6VuIeTJKEo9Uhi1KZjwdnUFAkdtvsEAqE9kCfR}
pwn.college{.TYImMWxzb8EV3hLmd79KKYiywFnQtgopwErvgXeLFd.LW-}
pwn.college{K3DGXH7TIFJ28ewWRP8MxCA79mHiD76vP4YljDKsNr89K6p}
pwn.college{B6tsFYaH8LgBI0Lor6x8eVGBWP144SrUt.928UHW8H7uhUJ}
pwn.college{B9.lYLCr81LmwuxWSAlN7CL.4HZMRl-liKn7.JClhNRx35N}
pwn.college{BnzAzFvRjoAp8-gx4Ctl0S70eEDHgoHNzl6zGLforqtaq-o}
pwn.college{2H4t8zQNiYVHprOK8wv93HaxI7IEUQ82ZSmty3JMoi6T9Q3}
pwn.college{bjEJwvzg9v2EuBjWSlcT7hI.R0.YgDyVIosUQZZmhRp2kNT}
pwn.college{cenulW0CcSW1uX0n0He.DWSXJy-uIwgqBYjiAnuF4IRwX30}
pwn.college{jWVXFXVP8BxiLlLryicC6ORdsybGfjovSeIb9Oe1C8dy3gk}
pwn.college{znoyOkbN4LqBJE5rTG1qm0dnn9rMhf0cpwcU37EcsWAaTS9}
pwn.college{2ITCjjvluyvx8htV0l6NWHaLdto2XA4gGrxbHjdr97UjbrE}
pwn.college{6pdrKZjO-JV1N-UG3TNmVwvFwNVSfIKbBQ7SLheS-UjRKCS}
pwn.college{1ad9VjZpq8l6wNESvpRAq4f7wpMNciIGW.qC3zb8dD5zaPp}
pwn.college{HV.D1VKhWq.5b1ul4-AWJkrUKEIbxNAivQ2A2x7ZW7iEx-l}
pwn.college{3v4KXAl6czy-5AL2A3pDIyYeauURqgcknA95TN1ebVtir58}
pwn.college{RZ0vnsW5h7dGM9DOUECRTFPVM.5Mb4zFZ4aL8T5lvp90wV6}
pwn.college{o8p-T41L3kNEMxOK9fKlxaKqHiReKadKOhVm3EwxOYal9Xj}
pwn.college{-wVGoShfABX7YE8LLFWKudCiXp27I9GUK7CzlwwLxQWapJk}
pwn.college{O26BvaSFB5sbzaXp.89I5VCMan2h2AKOSxzRXAhQyyxHe45}
pwn.college{TdU1APdKdBhySWVlfZILBo1OszBKw-cKMI4nn6-WicCm2go}
pwn.college{-XjydWra9komXdOCQOsTpvbKMIhEDIUFgv2DPOXJFJ4OrdF}
pwn.college{bp3HibbPFI5X7PwAHWMhxiMY.7x5R-zC0ZvKwXDSZaJV0Fi}
pwn.college{qWlweRTkRSUgfL.sXbT5hRGZDgY.cu2W8OpOYLIf5Y.ItmI}
pwn.college{azCO8vYS5vUY2xlgM69VB84jlde0DXL872BZLf1MCcdriiv}
pwn.college{ma224UQ22N9UfWzq19rVhLdqGMpAf774qEUfGJkKVX5MFlN}
pwn.college{Xdtdxt9n.-Q8-NM8LdYiy4XsdXOZIUVsWDQqGZRpkC79eOG}
pwn.college{0MiT8rfuwDA1mDsJpzCYLPJisYrWpSHSa2WDNXVR6OZiE30}
pwn.college{D4n5t6CpIlnKvofei7RC-ahgs2QcVTUR72L4gXjHgykOYgE}
pwn.college{p43fupfytuomf0oiIz4I1UgrnbesUp95SB4xs.pVACC.Ard}
pwn.college{BL7upoKtbczVSeFad.P0qaun0WrfVlCcVJIltxDwrCtQP3G}
pwn.college{k.ZudQvgctLp580CfKjAUxwX6Jce3I6el3XiQv5ukmlGARz}
pwn.college{WIulS1yOJ5TLwHf0Ur16pMsYhmCQeK9.XIvvYoNafXnsIbD}
pwn.college{chnheGk6ee18jjF7K44Y.klt6ul6Uvu3QdNed4BIADEdGyr}
pwn.college{fceWCcKHH5kD.sk7ktOGpLREzB8agI2tyMzdQMZoYBWD5BD}
pwn.college{v-VGYZApil0fK5zVJR2ATShyRD-pO36yst1PQBqQycpB9GV}
pwn.college{8X68sOf8Um3zY25nQHq.WelZWuGXSbL-7B-HZU48ECboWHT}
pwn.college{3B1nTssyDfu8ug9EwgUn8gSgxnIlZ7pcdzTvl.3ZnVcs7Jk}
pwn.college{TApWiJ8Q-VFRgESoIeU37nb0qQo.ZJrmZSTy8S.YT4PAHrU}
pwn.college{xTuhyKzhAAyfmz9PX.LbJDLV37hroN2-b6Mb4sEzWIWz9mj}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{ccWu59dbUlxYvoR6InX7QyQWYmQ.0FNzMDOxwCO1kjNzEzW}
```

## What I learned 
