# A Lightweight Dynamic Enforcement of Privacy Protection for Android


## The Language and the Policy
* [Lang.v](lib.lang.Lang.html): the syntax of the [language](lib.lang.Lang.html#lab3), 
    the [policy](lib.lang.Lang.html#lab2) and the
    [operational semantics](lib.lang.Lang.html#lab7) are defined here.
    Note that our program may consist of multiple processes.
## Static Checking and Program Translation
* [Typeinfer.v](lib.typechecking.Typeinfer.html): the [typing rules](lib.typechecking.Typeinfer.html#lab20) 
    and the [translation rules](lib.typechecking.Typeinfer.html#lab21) are
    defined here.

## The Soundness
* [LeakFree.v](lib.soundness.LeakFree.html): the leakage freedom property is
    defined here. It is a non-interference-like property, stating that 
    values of the variables not listed in the sending permission of process i,
    cannot affect the output influenced by the process i.
    In other words, process i does not send out the confidential data 
    unpermitted by its sending permission.
* [Sound.v](lib.soundness.Sound.html): the definition and proof of soundness are shown here. The
    soundness states that if the program is well-typed(i.e. it can be transformed
    to be an instrumented version), then it will not leak 
    any confidential information.
* [Simulation.v](lib.soundness.simulation.Simulation.html): the definitions of
    the [simulation between two process configuration](lib.soundness.simulation.Simulation.html#TSim) and
    the [simulation between two program configuration](lib.soundness.simulation.Simulation.html#PSim) are shown here.
    We use the *simulation* technique to help prove the non-interference.
* [Compositionality.v](lib.soundness.simulation.Compositionality.html): the
    definition and the proof of the [compositionality](lib.soundness.simulation.Compositionality.html#Compositionality) of the simulation are shown
    here. The compositionality states that if forall *i* such that the *i*th 
    process of program *p1* simulates the *i*th process of program *p2*,
    then *p1*  simulates *p2*.
    

The whole index of the coq files can be accessed [here ](index.html).

The whole proof can be download
[here](http://ssg.ustcsz.edu.cn/~zzp/research/android_security/android_security_proof.rar).
