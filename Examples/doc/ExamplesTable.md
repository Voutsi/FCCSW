List of Examples
===

## BASIC examples


|                      | [example_options.py](../options/example_options.py)         | [simple_workflow.py](../options/simple_workflow.py) | [simple_pythia.py](../options/simple_pythia.py)   | [particleGun.py](../../Generation/options/particleGun.py)                                                                         | [genJetClustering.py](../../Reconstruction/options/genJetClustering.py) |
|----------------------|-------------------------------------------------------------|-----------------------------------------------------|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| **input (alg)**      | reading events from a HepMC file                            | reading events from a HepMC file                    | generating PYTHIA events and saving them to HepMC | generating single particle events from a given list of types, with momentum, phi and theta from a given range, saving to HepMC | reading events from a HepMC file                                     |
| **other algorithms** |  dumping `HepMC::GenEvent`                                  | adding sample pile-up                 | converting `HepMC::GenEvent` to EDM               | dumping `HepMC::GenEvent`                                                                                                      | creating the histograms for HepMC                                    |
|                      | using dummy algorithm that creates EDM `fcc::JetCollection` | converting `HepMC::GenEvent` to EDM               | filtering MC particles                            | creating the histograms for HepMC                                                                                              | using sample jet clustering algorithm                                |
|                      |                                                             | using sample jet clustering algorithm          | using sample jet clustering algorithm             |                                                                                                                                | creating the histograms for jets                                     |
| **output (alg)**     | writing the EDM output to ROOT file using PODIO             | writing the EDM output to ROOT file using PODIO     | writing the EDM output to ROOT file using PODIO   | writing histograms to ROOT file                                                                                                | writing histograms to ROOT file                                      |


## SIMULATION examples


|                     | [PythiaDelphes_config.py](../../Sim/SimDelphesInterface/options/PythiaDelphes_config.py) | [geant_fullsim.py](../options/geant_fullsim.py)                                                                                 | [geant_pgun_fullsim.py](../options/geant_pgun_fullsim.py)                                                                      | [geant_fullsim_hcal.py](../../Sim/SimG4Components/tests/geant_fullsim_hcal.py)                                               | [geant_fullsim_gdml.py](../../Sim/SimG4Components/tests/geant_fullsim_gdml.py)                    | [geant_fastsim.py](../options/geant_fastsim.py)                                                                                                   |
|---------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| **events in HepMC** | generating PYTHIA events and saving them to HepMC             | reading events from a HepMC file                                                                                                | generating single particle events from a given list of types, with momentum, phi and theta from a given range, saving to HepMC | reading events from a HepMC file                                                                                          | reading events from a HepMC file                                                               | reading events from a HepMC file                                                                                                                  |
| **events in EDM**   |                                                               | converting `HepMC::GenEvent` to EDM                                                                                             | converting `HepMC::GenEvent` to EDM                                                                                            | converting `HepMC::GenEvent` to EDM                                                                                       | converting `HepMC::GenEvent` to EDM                                                            | converting `HepMC::GenEvent` to EDM                                                                                                               |
| **geometry**        |                                                               | geometry parsed from XML ([TestTracker.xml](../DetectorDescription/Detectors/compact/TestTracker.xml)) by DD4hep using `GeoSvc` | geometry parsed from XML ([TestHCal.xml](../DetectorDescription/Detectors/compact/TestHCal.xml)) by DD4hep using `GeoSvc`      | geometry parsed from XML ([TestHCal.xml](../DetectorDescription/Detectors/compact/TestHCal.xml)) by DD4hep using `GeoSvc` | geometry taken from [GDML file](../Sim/SimG4Common/gdml/example.xml) (no sensitive detectors!) |  geometry parsed from XML ([ParametricSimTracker.xml](../DetectorDescription/Detectors/compact/ParametricSimTracker.xml) by DD4hep using `GeoSvc` |
| **simulation**      | running Delphes simulation algorithm                          | FTFP_BERT physics list                                                                                                          | FTFP_BERT physics list                                                                                                         | FTFP_BERT physics list                                                                                                    | FTFP_BERT physics list                                                                         | FTFP_BERT physics list + `sim::FastSimPhysics` with parametrisation process                                                                       |
|                     |                                                               | empty action initialisation list                                                                                                | empty action initialisation list                                                                                               | empty action initialisation list                                                                                          | empty action initialisation list                                                               | action initialisation creates fast sim models                                                                                                     |
|                     |                                                               | saving tracker hits                                                                                                             | saving HCal hits                                                                                                               | saving HCal hits                                                                                                          |                                                                                                | saving smeared particles                                                                                                                          |
| **output**          | writing the EDM output to ROOT file using PODIO               | writing the EDM output to ROOT file using PODIO                                                                                 | writing the EDM output to ROOT file using PODIO                                                                                | writing the EDM output to ROOT file using PODIO                                                                           | writing the EDM output to ROOT file using PODIO                                                | writing the EDM output to ROOT file using PODIO                                                                                                   |