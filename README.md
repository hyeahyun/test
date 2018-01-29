

cmsrel CMSSW_8_0_20

cd CMSSW_8_0_20/src

cmsenv

git clone git@github.com:hyeahyun/test.git

mv pest/SUSYBSMAnalysis SUSYBSMAnalysis
 
scram b -j 4

cd SUSYBSMAnalysis/Zprime2muAnalysis/test/DataMCSpectraComparison

////////////////////////// If signal.. /////////////////////////////////

// After changing the sample pile path in the histosSimplified.py file,

cmsRun histosSimplified.py

// The zp2mu_histos.root file is created.


////////////////////////// If background.. /////////////////////////////////

//DY Dataset: /DYJetsToLL_M-50_TuneCUETP8M1_13TeV-amcatnloFXFX-pythia8/RunIISummer16MiniAODv2-PUMoriond17_80X_mcRun2_asymptotic_2016_TrancheIV_v6_ext2-v1/MINIAODSIM

//TTbar Dataset: /TTTo2L2Nu_TuneCUETP8M2_ttHtranche3_13TeV-powheg-pythia8/RunIISummer16MiniAODv2-PUMoriond17_80X_mcRun2_asymptotic_2016_TrancheIV_v6-v1/MINIAODSIM


//Changing the sample pile path in the histosSimplified.py file.

//After modifying storageSite in crabConfig.py and crabConfig_TT.py, submit crab job


//DY sample

crab submit -c crabConfig.py


//TTbar sample

crab submit -c crabConfig_TT.py


