# metLab
An R-package designed to use with he combined targeted &amp; non-targeted (TNT) metabolomics method described in Ribbenstedt et al. 2018
but which might come in handy for anyone working with Liquid Chromatography Mass Spectrometry (LC-MS) data.

The functions included in this package are:

"reorgXcalArea" and "reorgXcalConc"
- Restructuring excel-files generated by Thermo XCalibur Quan Browser, resaved in .xlsx-format, into a single worksheet .xlsx file.
  Choose between extracting the area or the concentrations from your output-file.

"fullDecon"
- Isotopically deconvoluting Flow Injection-MS (FI-MS) lipidomics data; removing the isotopic influence of lower mass lipids on the signals
  of lipids which weight 2-10 a.u. or m/z or etc. more. Only works when chromatograms are overlapped, as they are in FI-MS where no
  column is employed. Designed to take the output format from the "reorgXcal" functions and do the deconvolution for all samples and
  lipids specified in separate setting files.
  
"lipFragMatch"
- Takes Orbitrap XIC-data for any kind of fragment known to be shared by a group of compounds (such as 184 m/z for phosphatidyl
  cholines and sphingomyelins), matches those MS2-fragments against the retention time (RT) of MS1-ions which have been matched against
  a "LIPID maps" exact mass offline database. Will implement settings for how precise the script is in the future. For the moment it's
  set to match RTs within +/- 0.5 minutes for MS2-fragments and MS1 parent ion m/z's. For MS1's in the mass-list and the
  mass now connected to the RT +/- 0.05 m/z is the standard setting for now.
  
 All other functions in the package are at the moment experimental and unfinished.
