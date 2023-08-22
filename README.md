# pfnano-prod

Submit crab jobs for PFNano production using crabb.py.

Step 1: setup the PFNano (current branch: `12_6_0`, please *double-check the branch is correct*)
 according to https://github.com/cms-jet/PFNano/tree/12_6_0#recipe

Step 2: setup `pfnano-prod`

```bash
mkdir $CMSSW_BASE/src/PhysicsTools/PFNano/production
cd $CMSSW_BASE/src/PhysicsTools/PFNano/production
git clone https://github.com/colizz/pfnano-prod.git -b nanov11 . ## make sure to use nanov11 branch!!!
```

Step 3: submit crab jobs configured in `crab_ymls/`.

See introducitons in https://github.com/cms-jet/PFNano/tree/12_6_0#submission-to-crab.
Also, remember to edit the LFN path and storage cite in the config.

```bash
python3 ../test/crabby.py -c crab_ymls/XXX --make
```
Then append `--submit` for submission.

