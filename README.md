# Physc-15c-Final-PCT-project
#### Jacob Nie, Justin Hsu, Linda Jin

Final report for group The Wednesdays's point contact transistor.

## TRANSISTOR FUNDAMENTALS

Since their invention in the mid-20th century, transistors have completely revolutionized the electronics and information landscape. The transistor is widely considered to be the most important invention of the 20th century. Every communications and computing device operates with the function of the transistor. 

The two key characteristics of a transistor are signal amplification and current on-off switching. Although there are many different kinds of transistors that rely on markedly different principles of semiconductor physics, they all have these two abilities. In all transistors, a voltage from an input circuit (the base terminal) changes the effective resistance between the collector and emitter terminals. 

![amplification](https://raw.githubusercontent.com/Klinjin/Physc-15c-Final-PCT-project/main/transistor.png)

This can amplify a signal: a weak signal can power the input circuit, changing the voltage of the base terminal. The output circuit for the collector and emitter terminals can have a very large voltage source. Even if the resistance between the collector and emitter terminals is weakly varied, a large variation in current can be generated, leading to a large power amplification compared to the input circuit. This is why transistors are ubiquitous in all communications devices that rely on receiving and transmitting signals.

The same principle can also be used to implement on-off switching: changing the base voltage from 0 to V will switch the current from the collector to emitter terminals either on or off. This fact is why transistors can be used to realize digital logic. Thus, any modern day computer contains billions of transistors, each of them on the nanometer scale. 

## TRANSISTOR HISTORY

The fundamental transistor design implemented on modern day circuit boards is the field-effect transistor (FET). 

![fet](https://raw.githubusercontent.com/Klinjin/Physc-15c-Final-PCT-project/main/fig1.png)

A metal gate separated from the semiconductor layer by an oxide layer can remotely change the carrier concentration in the semiconducting layer. A voltage on the metal gate can induce a change in charge density in the semiconductor by relying on their mutual capacitance. Thus, the conductivity between the source and drain terminals can be changed remotely using the gate terminal, achieving the transistor function.

But prior to the invention of the FET, most transistors were junction transistors. The first of these was the bipolar junction transistor (BJT), invented by William Shockley in 1948.

![bjt](https://raw.githubusercontent.com/Klinjin/Physc-15c-Final-PCT-project/main/npn.png)

The input circuit controls the voltage applied to the base, V_BE. This varies the current that flows between the collector and the emitter. When the voltage to the base is zero, the output circuit, between the collector and the emitter, consists of two back to back diodes in opposite directions. As a result, very little current flows. When there is a non-zero voltage applied to the base, the base-emitter p-n junction becomes forward biased. Then electrons will flow from the first n-region to the p-region. If the p-region is sufficiently thin, the majority of these electrons will diffuse all the way to the second n-region. These diffusing electrons form the collector current. The remaining electrons recombine with holes in the p-region and form the base current. If the transistor design is optimized, the collector current can exceed the base current by several orders of magnitude, achieving a strong amplification going from the input to the output circuit.

Although the BJT was one of the first transistors ever invented, it was not the very first. The precursor to the BJT, invented by the same people (Shockley’s group), was the point contact transistor (PCT). 

![pct](https://raw.githubusercontent.com/Klinjin/Physc-15c-Final-PCT-project/main/pct.png)

The point contact transistor consisted of a block of majority n-doped germanium with a thin p-doped region on the surface. The bottom is connected to the base terminal, and two gold contacts placed very closely next to each other on the p-doped region form the emitter and collector terminals. In 1947, Brattain and Bardeen, working under Shockley at Bell Labs, successfully demonstrated transistor amplification for the first time using this setup. This discovery won them the Nobel Prize in physics. Due to the impracticality of this setup, the design was quickly replaced by the BJT, which was structurally and electronically much more reliable. Despite being the first transistor design, the PCT never received full commercialization. Its physical function has not been carefully researched, and there remain some mysteries behind why it works in the first place. Hence, we do not make an attempt to explain how it works.

However, in trying to build a home-made transistor, the PCT remains as an attractive starting point, especially considering its historical significance. Unlike all other transistor designs, which require careful growth and doping regimens, the PCT builds upon simple germanium p-n junctions, which are found in any cheap germanium diode. 




## THE GERMANIUM DIODE
Early semiconductor developments used germanium
as the commercial semiconductor material however was
eventually replaced by silicon. However, germanium
diodes have the advantage of an intrinsically low forward
voltage drop, typically 0.3 volts; this low forward volt-
age drop results in a low power loss and more efficient
diode.[1] Hence, we used a germanium diode as the source
of semiconductor to build our device on.The diode looks
like Figure. 1.

![fullDiagram](https://user-images.githubusercontent.com/102839205/171823949-86059013-235c-4df7-91c3-73513a020ae3.jpg)

The diode was broken carefully with a cutting pliers.
Using a microscope, we were able to guess the structure of
the germanium diodes we purchased. We demonstrated
that we could reliably and reproducibly crack open diodes
to reveal the Ge p-n junction inside.
The orange side has an obvious square block of metal
(Figure. 2a), which is different from the round conductor
on the black side of the glass (Figure. 2b). We deduced
that the metal block is the germanium, with the approx-
imate size of 0.3mm × 0.3mm through 10x image on mi-
croscope. We can see the relative sizes of the tentative
germanium block and the metal base in Figure .2d.
<img width="511" alt="截屏2022-06-03 上午1 54 15" src="https://user-images.githubusercontent.com/102839205/171824249-1fb1a07f-ec0d-431e-a945-c11a6000c7af.png">

The diode structure can hence be anticipated as a small
germanium block in contact with two larger metal con-
ductor bases. The anticipated inner structure is plotted
in Figure. 3.

![structure](https://user-images.githubusercontent.com/102839205/171824363-6b7fca27-92a9-49a7-83db-8ef2f0faa78f.png)

This small block of germanium is what we needed for
a P-N junction on semiconductor as one side is P-doped
and the other is N-doped. Based on this existed structure, we came to perceive our fabrication plan for a bipo-
lar P-N-P transistor.


## TESTING THE CUT-OPEN DIODE

We proved that the metal block is indeed germanium by putting an exterior contact on it. By measuring the current and forward voltage of the circuit of both an intact diode and the cut one with the same resistor, we can see they behave the same. 

 Forward-biased I-V curve of intact Ge diode |  Forward-biased I-V curve of cut Ge diode
:-------------------------:|:-------------------------:
![unnamed-3](https://user-images.githubusercontent.com/102839205/171825211-e5f72332-6e4f-4b2e-baa9-658ff21afa54.png) | ![unnamed-4](https://user-images.githubusercontent.com/102839205/171825235-0e19c7b8-c42c-421e-9b5f-0da2cd054c49.png)
![unnamed](https://user-images.githubusercontent.com/102839205/171825358-5f8f40e6-297a-493b-a237-7816014ff110.png) | ![unnamed-2](https://user-images.githubusercontent.com/102839205/171825376-883bab70-8992-405a-8a84-90fc3ccb59a1.png)

## Fabrication Process: Difficulties & Solutions
Instead of only one p-n junction we need two for a p-n-p transistor. We can achieve this by etching a thin scratch on the germanium. But considering the size of the germanium and stabilizing the two pins to keep in contact with the germanium without touching each other, we need a better plan for the feasibility and the unity of the device.
Initial Plan
:-------------------------:
![unnamed-5](https://user-images.githubusercontent.com/102839205/171825780-99aac7ea-5fa9-487b-89d4-c6cb43a2969f.png)|


Hence, another essential issue is to establish the micropositioning on x-y-z axes. We solved the problem of micromanaging the two pins as a whole entity by hot gluing them together. The conductor has insulating coating, so we kept the parts inside the **hot-glued tube** insulated and sanded the two ends of the wires to conduct current across. Another challenge arise when the two contact points are too close to each other, they may not be detached. So we cut the excess sanded part to make sure only the cross section contacts with the germanium is conductive. The resistance between two ends on the other side of the hot-glued tube was measured to be zero, so disconnected between two terminals.

<img width="792" alt="截屏2022-06-03 上午2 17 47" src="https://user-images.githubusercontent.com/102839205/171826358-ecf2f6ee-8563-4b9d-80f6-6b8096fc0545.png">

Two hot-glued terminals in contact with the germanium, stabilized together by a tape.
:-------------------------:
![T20220525_001_0001](https://user-images.githubusercontent.com/102839205/171826908-b02a3f55-5dc7-4c07-9158-ca8dfee5aa57.jpg)|

Another detail is that the conductor is very thin so even easier to break after being sanded. The hot glue protects the wires. The wires were soldered to jumper wires for taking measurements through LabJack, and heat shrink tube was also used to protect the fragile device,
<img width="792" alt="截屏2022-06-03 上午2 26 10" src="https://user-images.githubusercontent.com/102839205/171827860-8b9caa78-21c2-4945-85bd-6afd4b5e1396.png">

## PERFORMANC
[justin]

## FUTURE IMPROVEMENTS
[justin]
