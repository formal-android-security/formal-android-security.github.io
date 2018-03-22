# A Lightweight Dynamic Enforcement of Privacy Protection for Android


## The Language and the Policy
* [Lang.v](doc/lib.lang.Lang.html): the syntax of the [language](doc/lib.lang.Lang.html#lab3), 
    the [policy](doc/lib.lang.Lang.html#lab2) and the
    [operational semantics](doc/lib.lang.Lang.html#lab7) are defined here.
    Note that our program may consist of multiple processes.
## Static Checking and Program Translation
* [Typeinfer.v](doc/lib.typechecking.Typeinfer.html): the [typing rules](doc/lib.typechecking.Typeinfer.html#lab20) 
    and the [translation rules](doc/lib.typechecking.Typeinfer.html#lab21) are
    defined here.

## The Soundness
* [LeakFree.v](doc/lib.soundness.LeakFree.html): the leakage freedom property is
    defined here. It is a non-interference-like property, stating that 
    values of the variables not listed in the sending permission of process i,
    cannot affect the output influenced by the process i.
    In other words, process i does not send out the confidential data 
    unpermitted by its sending permission.
* [Sound.v](doc/lib.soundness.Sound.html): the definition and proof of soundness are shown here. The
    soundness states that if the program is well-typed(i.e. it can be transformed
    to be an instrumented version), then it will not leak 
    any confidential information.
* [Simulation.v](doc/lib.soundness.simulation.Simulation.html): the definitions of
    the [simulation between two process configuration](doc/lib.soundness.simulation.Simulation.html#TSim) and
    the [simulation between two program configuration](doc/lib.soundness.simulation.Simulation.html#PSim) are shown here.
    We use the *simulation* technique to help prove the non-interference.
* [Compositionality.v](doc/lib.soundness.simulation.Compositionality.html): the
    definition and the proof of the [compositionality](doc/lib.soundness.simulation.Compositionality.html#Compositionality) of the simulation are shown
    here. The compositionality states that if forall *i* such that the *i*th 
    process of program *p1* simulates the *i*th process of program *p2*,
    then *p1*  simulates *p2*.
    

The whole index of the coq files can be accessed [here ](doc/index.html).

The whole proof can be download
[here](https://raw.githubusercontent.com/formal-android-security/formal-android-security.github.io/master/coq_proof_8.7.zip).
Please compile the coq files with Coq 8.7.0 version.
