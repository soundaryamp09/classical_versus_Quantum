# classical_versus_Quantum
unstructred search:
           is like guessing a key number between 1 to 100 and the wrong guess won't give correct answer in the worst case we would have 99 calls to our classical oracle in order to find the solution ie the key number

In an example of unstructred search we dont get any information from previous guesses about the correct guesses about what the correct solution is o(N) times to locate an item within this database size N with N being the number of item that we are searching through
![image](https://github.com/soundaryamp09/classical_versus_Quantum/assets/122505807/e4b89fde-9495-4964-9880-aa7e706b252a)

#Quantum Solution :
Grover Algorithm use superposition of qubit and phase interference to improve unstructured database search from O(log(N)) to O(Sqrt(N))
  * Amplitude amplification: this allows us to increase the probability og observing the correct answer or the object of the search.
    **incresing ** the probability amplitude of answer kit and **decrese** all other probability amplitude.
    **procedure** :
    Step-1: start with a balanced superposition
    Step-2:Assign negative phase for chosen ket let's say |11>(use controlled Z-gate)
    ![image](https://github.com/soundaryamp09/classical_versus_Quantum/assets/122505807/c0b17209-ed90-497c-8da9-6ee5d724ae74)

    Step-3:invert all amplitudesaround mean (this will run for Sqrt(N) times)

    *identify your seach problem and the data(N items) you wish to seacrch
    * find the smallest number n that satisfies N<=2^n  (hadamard gate allows us to look all values at once)
    * construct oracle, fand gate/matrix U , that flip the sign of the object of Seach
    * Run U(f) , that flips the sign of the object of Search followed by U(phi) the circuit that inverts around the mean(Grover Diffusion Operator).Repeate this Sqrt(N) times
      ![image](https://github.com/soundaryamp09/classical_versus_Quantum/assets/122505807/21a4b891-86d3-4ca1-bfc2-ca3a8d98ef6a)
      ![image](https://github.com/soundaryamp09/classical_versus_Quantum/assets/122505807/782383b8-45ee-4ef3-b376-e71737739351)


    * measure and read off the state with an encoding that corresponds to the desired item in the database.Map the resulting state back to the data.
    * ![image](https://github.com/soundaryamp09/classical_versus_Quantum/assets/122505807/30b39612-e786-4901-9341-c60da08d563f)


    
    
