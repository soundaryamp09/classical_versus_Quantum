# classical_versus_Quantum
unstructred search:
           is like guessing a key number between 1 to 100 and the wrong guess won't give correct answer in the worst case we would have 99 calls to our classical oracle in order to find the solution ie the key number

In an example of unstructred search we dont get any information from previous guesses about the correct guesses about what the correct solution is o(N) times to locate an item within this database size N with N being the number of item that we are searching through

#Quantum Solution :
Grover Algorithm use superposition of qubit and phase interference to improve unstructured database search from O(log(N)) to O(Sqrt(N))
  * Amplitude amplification: this allows us to increase the probability og observing the correct answer or the object of the search.
    **incresing ** the probability amplitude of answer kit and **decrese** all other probability amplitude.
    **procedure** :
    Step-1: start with a balanced superposition
    Step-2:Assign negative phase for chosen ket let's say |11>(use controlled Z-gate)
    Step-3:invert all amplitudesaround mean (this will run for Sqrt(N) times)

    *identify your seach problem and the data(N items) you wish to seacrch
    * find the smallest number n that satisfies N<=2^n  (hadamard gate allows us to look all values at once)
    * construct oracle, fand gate/matrix U , that flip the sign of the object of Seach
    * Run U(f) , that flips the sign of the object of Search followed by U(phi) the circuit that inverts around the mean(Grover Diffusion Operator).Repeate this Sqrt(N) times
    * measure and read off the state with an encoding that corresponds to the desired item in the database.Map the resulting state back to the data.
    * ![image](https://github.com/soundaryamp09/classical_versus_Quantum/assets/122505807/30b39612-e786-4901-9341-c60da08d563f)


    
    
