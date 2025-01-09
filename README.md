# AccSiM: State-Aware Simulation Acceleration for Simulink Models

Each folder in this repository represents a benchmark model, containing the model file and its corresponding generated executable files in the AccSiM folder.

## AccSiM Folder

The AccSiM folder contains two essential executable files:

- `SimuTest.exe`: Used for code simulation.
- `CovTest.exe`: Employed for coverage collection.

### Simulation

To obtain simulation duration, use the provided script, `Simulation.bat`, which will execute `SimuTest.exe`.  <br>
It's crucial to edit the script's line 3 to customize execution parameters. For example:

```bash
SimuTest.exe -b <TestFilePath> -s <TotalSimulationSteps>
```

Replace '&lt;TestFilePath&gt;' with the actual path to your test file. The test file is expected to be in binary (.bin) format, with test case of each simulation step organized in groups, tightly packed without gaps.<br>
The '&lt;TotalSimulationSteps&gt;' should match the step number in your test file.<br><br>

NOTE that this example is suitable ONLY for Windows 11. <br>
For Windows 10 or lower versions, please use the FULL PATH for both 'SimuTest.exe' and '&lt;TestFilePath&gt;'.<br>

### Coverage

To obtain coverage information, use the provided script, `Coverage.bat`, which will execute `CovTest.exe`.  <br>
It's essential to edit the script's line 1 to customize execution parameters. For example:

```bash
CovTest.exe -b <TestFilePath>
```


## CSEV: Charging System of Electric Vehicles

This is the benchmark model used as case study for diagnostic function in our paper.<br>
Apart from the original model file, `CSEV_Error_Injected.slx` stands for the model file we manually inject errors into.<br><br>

To obtain diagnostic results, we provide the `Diagnosis.bat` script for executing `DiagTest.exe`, which corresponds to the executable file associated with `CSEV_Error_Injected.slx`.<br>
The usage is consistent with the 'Simulation.bat' above.<br>
