PUBLICATIONS:
Lucey, K.J., Kuzniar, R.L., and Caldwell, J.P., 1995, Hydrogeology and water
quality of the Mississippi River alluvium near Muscatine, Iowa, June 1992
through June 1994: U.S. Geological Survey Water-Resources Investigations
Report 95-4049, 74 p., 1 pl., https://doi.org/10.3133/wri954049.

Lucey, K.J., 1997, Evaluation of drawdown and sources of water in the
Mississippi River alluvium caused by hypothetical pumping, Muscatine, Iowa:
U.S. Geological Survey Water-Resources Investigations Report 97-4162, 18 p.,
https://doi.org/10.3133/wri974162.

Savoca, M.E., Lucey, K.J., and Lanning, B.D., 2002, Simulation of ground-water
flow and delineation of areas contributing recharge to municipal water-supply
wells, Muscatine, Iowa: U.S. Geological Survey Water-Resources Investigations
Report 2002-4004, 26 p., https://doi.org/10.3133/wri024004.

ARCHIVE HISTORY:
199602   WRIR 95-4049 model archive created
199712   WRIR 97-4162 model archive created
199907   WRIR 02-4004 project files organized (readme.muscatine, 7/27/99)
202611   Files assembled into this package from the three archives above;
         readme.txt, georef files, grid shapefiles, and report PDFs added.
         Original files were copied without modification except for the
         removal of personal and internal information described in
         "Removal of personal and internal information" below.

DISCLAIMER:
------------------------------------------------------------------------------
  UNLESS OTHERWISE STATED, ALL DATA, METADATA AND RELATED MATERIALS ARE
  CONSIDERED TO SATISFY THE QUALITY STANDARDS RELATIVE TO THE PURPOSE FOR
  WHICH THE DATA WERE COLLECTED. NO WARRANTY EXPRESSED OR IMPLIED IS MADE
  REGARDING THE DISPLAY OR UTILITY OF THE DATA FOR OTHER PURPOSES, NOR ON ALL
  COMPUTER SYSTEMS, NOR SHALL THE ACT OF DISTRIBUTION CONSTITUTE ANY SUCH
  WARRANTY.

  THE FILES CONTAINED HEREIN ARE PROVIDED AS A CONVENIENCE TO THOSE WHO WISH
  TO REPLICATE SIMULATIONS OF GROUNDWATER FLOW THAT ARE DESCRIBED IN U.S.
  GEOLOGICAL SURVEY WATER-RESOURCES INVESTIGATIONS REPORTS 95-4049, 97-4162,
  AND 02-4004.

  ANY CHANGES MADE TO THESE FILES COULD HAVE UNINTENDED, UNDESIRABLE
  CONSEQUENCES. THESE CONSEQUENCES COULD INCLUDE, BUT MAY NOT BE LIMITED TO:
  ERRONEOUS MODEL OUTPUT, NUMERICAL INSTABILITIES, AND VIOLATIONS OF
  UNDERLYING ASSUMPTIONS ABOUT THE SUBJECT HYDROLOGIC SYSTEM THAT ARE INHERENT
  IN RESULTS PRESENTED IN THE REPORTS LISTED ABOVE.

  THE U.S. GEOLOGICAL SURVEY ASSUMES NO RESPONSIBILITY FOR THE CONSEQUENCES OF
  ANY CHANGES MADE TO THESE FILES. IF CHANGES ARE MADE TO THE MODEL, THE USER
  IS RESPONSIBLE FOR DOCUMENTING THE CHANGES AND JUSTIFYING THE RESULTS AND
  CONCLUSIONS.

  THESE FILES WERE CREATED BETWEEN 1993 AND 2002 ON COMPUTER SYSTEMS THAT ARE
  NO LONGER IN USE. THE MODELS HAVE NOT BEEN RERUN WITH CURRENT SOFTWARE AS
  PART OF ASSEMBLING THIS PACKAGE. SEE "NOTES ON RERUNNING THE MODELS" BELOW.
------------------------------------------------------------------------------

DESCRIPTION:
----------------------------------------------------------------------------
This package contains three generations of a steady-state MODFLOW
groundwater flow model of the Mississippi River alluvial aquifer near
Muscatine, Iowa (USGS Iowa District projects 4619-07300 and 4619-07700). All
models have three layers (layer 1 = upper alluvium, layer 2 = lower
alluvium, layer 3 = bedrock), use units of feet and days, and simulate
steady-state conditions.

1. 1995 model (WRIR 95-4049), directory .\wrir95-4049\
   Calibrated steady-state model of February 1993 hydrologic conditions.
   MODFLOW version: MODFLOW-88 (McDonald and Harbaugh, 1988), USGS
   distribution of June 1994 (source code in .\wrir95-4049\source\ and
   .\wrir97-4162\source\), with BCF3 (7/9/92) and the Stream Package STR1
   version 2 (12/18/90; Prudic, 1989).
   30 rows x 24 columns, 2,000-ft by 2,000-ft cells. MODFLOW packages:
   BAS1, BCF3, WEL1, DRN1, RIV1 (Mississippi River), GHB1, RCH1, STR1
   (stream package, used for Muscatine Slough and streams), SIP1 (closure
   criterion 0.001 ft), OC. Also includes runs without pumping and of
   drawdown caused by February 1993 pumping, and post-processing for RMSE,
   subregional water budgets (ZONEBUDGET), and VCONT calculation.

2. 1997 pumping scenarios (WRIR 97-4162), directory .\wrir97-4162\
   MODFLOW version: same as the 1995 model (MODFLOW-88, USGS distribution
   of June 1994).
   The 1995 model, unchanged except for well pumpage and solver settings,
   used to simulate drawdown and sources of water for hypothetical pumping
   scenarios: 1 Grandview, 2 Progress Park, 3 North, 4 West, 5 South, and a
   cumulative scenario with all five. The scenarios use an SIP closure
   criterion of 0.01 ft instead of 0.001 ft (see
   .\wrir97-4162\input\describes.runs). An additional scenario that was not
   published in WRIR 97-4162 (scen99) is included in
   .\wrir97-4162\unpublished_scen99\.

3. 1999 model (WRIR 02-4004), directory .\wrir02-4004\
   The 1995 model rebuilt in the Groundwater Modeling System (GMS) with
   305 rows x 250 columns of 200-ft by 200-ft cells, recalibrated, and used
   with MODPATH to delineate areas contributing recharge and 2-,
   5-, and 10-year zones of transport for municipal well fields.
   MODFLOW version: MODFLOW-88 (McDonald and Harbaugh, 1988) as
   distributed with GMS version 2.1, with the same package versions as the
   1995 model (BAS1, BCF3 7/9/92, STR1 version 2 12/18/90); source code for
   the GMS executable is not included.
   MODPATH version: MODPATH 3.00 (Release 1, 9-94; Pollock, 1994).
   Simulations provided:

     mod99f     1998 average pumpage (55 wells, 6,795,100 ft3/d); the
                primary model of the report
     mod99f93   February 1993 pumpage (54 wells, 6,149,690 ft3/d)
     mod99lf    1998 pumpage with recharge from precipitation decreased by
                20 percent (less-than-normal recharge, report fig. 14)
     mod99mf    1998 pumpage with recharge from precipitation increased by
                20 percent (greater-than-normal recharge, report fig. 14)

   Effective porosity used by MODPATH: 0.15 to 0.24 in layer 1, 0.15 to
   0.20 in layer 2, and 0.03 in layer 3 (WRIR 02-4004).

Each of the 1995 and 1997 directories is the original USGS model archive,
copied with its original layout (ancillary, contents, input, output,
source).

NOTE: The original readme and description files from the model archives are
included unchanged except for the removal of internal file paths and
personal information (see "Removal of personal and internal information"
below). These files may not be correct, because of errors in the original
documentation and because some files were reorganized or not included when
this package was assembled. Where the original files and this readme
differ, the file listings in this readme reflect the files actually
present.

MODEL GEOREFERENCE:
----------------------------------------------------------------------------
Both model grids are in Universal Transverse Mercator (UTM) zone 15 north,
North American Datum of 1927 (Clarke 1866 spheroid), in U.S. survey feet.
Elevations are in feet above the National Geodetic Vertical Datum of 1929.
Both grids are rotated 1.2 degrees counterclockwise about the lower-left
(southwest) corner. Row 1 is the northern edge and column 1 is the western
edge of each grid.

  Model    Rows x cols  Cell (ft)  Origin x (ft)   Origin y (ft)   Rotation
  1995     30 x 24      2,000      2,140,141.92    14,986,602.54   1.2 deg
  1999     305 x 250    200        2,139,000.00    14,986,450.00   1.2 deg

Corner coordinates, latitudes and longitudes, and verification notes are in
.\georef\modelgeoref_1995_2000ft_grid.txt and
.\georef\modelgeoref_1999_200ft_grid.txt. Polygon shapefiles of both grids,
with row, column, and IBOUND attributes, are in .\georef\.

SYSTEM REQUIREMENTS AND ORIGINAL COMPUTING ENVIRONMENT:
----------------------------------------------------------------------------
1995 and 1997 models: run on a Data General AViiON (Motorola 88000) UNIX
workstation with the USGS version of MODFLOW dated June 1994 (MODFLOW-88
with packages documented through June 1994; see
.\wrir95-4049\source\readme.text). The run files are Bourne shell (sh)
scripts. The compiled executables in this package (ancillary\contour,
ancillary\vcontcalc\vcont) are Data General m88k binaries and will not run
on current computers.

1999 model: built with GMS version 2.1 (Brigham Young University /
Environmental Modeling Systems), with model files written in MODFLOW-88
package formats and managed through GMS "super files" (*.mfs). Simulations
mod99f and mod99f93 were last run under Windows NT; mod99lf, mod99mf, and
all MODPATH runs were run on a Sun UNIX workstation with the MODFLOW and
MODPATH executables distributed with GMS.

NOTES ON RERUNNING THE MODELS:
----------------------------------------------------------------------------
The models have not been rerun with current software, and no technical
support is provided for rerunning them. Users who wish to rerun or convert
the models should be aware of the following:

* The original UNIX shell scripts (*.run, *.in, contour.dd, and
  modflow.csh) were written for the Data General and Sun workstations
  used in the 1990s. They call executables that are not included or
  will not run on current computers (MODFLOW, contour, rmse, ZONEBUDGET),
  a plotter and printer, and a text editor, and they rely on UNIX file
  links. They will not run on Windows and are not expected to run
  without modification on any current computer. They are included for
  completeness, as a record of how the models were run.

* The MODFLOW source code provided is the June 1994 USGS version. The
  source files in .\wrir97-4162\source\ form the complete set; the set in
  .\wrir95-4049\source\ lacks several package files that the main program
  references.

* Binary output files (heads, drawdown, and cell-by-cell budgets) were
  written in the byte order of the computer that created them. Files from
  the 1995 and 1997 models, the 1999 simulations mod99lf and mod99mf, and
  all MODPATH files are big-endian; the 1999 simulations mod99f and
  mod99f93 are little-endian.

* The archived listing files (*.out) contain the original simulated heads
  and water budgets and can be used to check any rerun or conversion.

REMOVAL OF PERSONAL AND INTERNAL INFORMATION:
----------------------------------------------------------------------------
The following changes were made to the original files when this package
was assembled (November 2026). Model input and simulated results were not
changed.

  * Internal server directory paths (for example, paths on the original
    UNIX and Windows NT file servers) were replaced with relative names
    of the same length ("./name" followed by spaces) in all text files,
    model listing-file headers, MODPATH response and summary files, ARC
    Macro Language scripts, and ARC/INFO table definitions. Binary MODFLOW
    output files were not changed.
  * Contact names and telephone numbers were removed from the supply-well
    tables (.\wrir02-4004\ancillary\well_data\supplywells\supwells.*).
  * A contact name, telephone number, and user name were blanked in the
    ARC/INFO documentation tables for the Iowa outline coverage
    (.\wrir02-4004\gis\coverages\info\). A user name was replaced in the
    INFO command file attload.comi.
  * Author metadata was removed from the two .docx files in .\wrir97-4162\.
  * ARC/INFO coverage processing logs (files named "log"), ArcView project
    files (*.apr), an internal memorandum (coverages\initarc.doc), and a
    contact list (musc077\arch_list.077) were not included.
  * Project correspondence, contact lists, and contaminant-source
    inventories from the original project directories were not included.

All GIS layers were checked after these changes and read identically to
the original files with GDAL/OGR.

FILE CONTENTS:
   ----------------------------------------------------------------------------
   The files in each directory are described below by directory and
   subdirectory. UNIX shell scripts listed below are included for
   completeness and will not run on current computers without
   modification (see "Notes on rerunning the models").

   \muscatine_gw_models\ directory contains this readme file and all
   directories of this package.

   1. .\readme.txt   This file. Documents the structure, directories, and
                      file descriptions of this package, and notes on
                      rerunning the models.

Files in directories include the following:

   A. .\georef\ directory contains georeference information for the model
      grids (10 files)

      modelgeoref_1995_2000ft_grid.txt  georeference of the 1995 grid (used
                                         in WRIR 95-4049 and 97-4162)
      modelgeoref_1999_200ft_grid.txt   georeference of the 1999 grid (used
                                         in WRIR 02-4004)
      model1995_grid.{shp,shx,dbf,prj,cpg}
                                        polygon shapefile of 1995 model
                                         cells (720 cells), attributes row,
                                         col, ibound_l1-l3, active
      model1999_grid.{shp,shx,dbf,prj,cpg}
                                        polygon shapefile of 1999 model
                                         cells (76,250 cells), attributes
                                         row, col, ibound_l1-l3, active

   B. .\report\ directory contains the published reports (4 files)

      WRIR_954049.pdf           WRIR 95-4049 (Lucey and others, 1995)
      WRIR_954049_plate.pdf     WRIR 95-4049, plate 1
      WRIR_974162.pdf           WRIR 97-4162 (Lucey, 1997)
      WRIR_02-4004.pdf          WRIR 02-4004 (Savoca and others, 2002)

   C. .\wrir95-4049\ directory contains the original model archive for
      WRIR 95-4049. See README.txt and contents\descriptions in this
      directory for the original file-by-file descriptions.

      README.txt                original description of subdirectories and
                                 files

      1. .\ancillary\ directory contains post-processing input, run, and
         output files (27 files, 1 directory)

         contour                 USGS contour plotting program (Data
                                  General executable; not runnable)
         contour.dd              UNIX shell (sh) commands that contour
                                  drawdown (unfmt.dd) for the 3 layers
                                  with the contour program and print the
                                  plots
         contour.in              UNIX shell (sh) commands that contour
                                  simulated heads (unfmt.head) for the 3
                                  layers and print the plots
         rmse.dat                measured water levels for RMSE comparison
         rmse.f                  Fortran source for RMSE program (P. Tucci)
         rmse.in                 UNIX shell (sh) commands that run the
                                  rmse program
         rmse.out                comparison of measured and simulated water
                                  levels and RMSE by layer
         unfmt.budg              copy of cell-by-cell budget used by
                                  zonebudget runs
         unfmt.nopmp.budg        copy of no-pumping cell-by-cell budget
         zonebud.f               Fortran source for ZONEBUDGET
         zone*.dat               zone arrays: bluff (zonebluff), three
                                  hydrologic zones (zonehyd), induced
                                  river flow (zoneinduce), river cells
                                  (zoneriv)
         zone*.in                UNIX shell (sh) commands that run
                                  ZONEBUDGET and print the output
         zone*.out*              ZONEBUDGET output, including sensitivity
                                  runs (bedrock T = 10 and 200 ft/d;
                                  river conductance and VCONT x 0.1, x 10)

         a. .\vcontcalc\ directory contains the VCONT program from S. Leake
            (USGS Arizona) and its input and output (13 files)

            READ.ME              description of the VCONT program and files
            leake.*              input arrays (layer tops, bottoms,
                                  hydraulic conductivity, layer 3
                                  transmissivity, ibound of Pennsylvanian
                                  rocks)
            vcont                Data General executable (not runnable)
            vcont.f              Fortran source
            vcont1, vcont2       calculated VCONT arrays, layers 1-2 and
                                  2-3
            vcont.calc.sas       SAS program for VCONT of Pennsylvanian
                                  rock wedge

      2. .\contents\ directory contains original documentation (3 files)

         descriptions            descriptions of subdirectories and files
         instructions            instructions for running the model and
                                  post-processing programs
         reference               citation for WRIR 95-4049

      3. .\input\ directory contains MODFLOW input for the final steady-
         state model (14 files)

         finalss.bas             Basic Package (BAS1)
         finalss.bcf             Block-Centered Flow Package (BCF3)
         finalss.drn             Drain Package
         finalss.gh              General-Head Boundary Package
         finalss.oc              Output Control
         finalss.rch             Recharge Package
         finalss.riv             River Package (Mississippi River)
         finalss.sip             Strongly Implicit Procedure solver
         finalss.strm            Stream Package (STR1)
         finalss.wel             Well Package, February 1993 pumpage
         finalss.run             UNIX shell (sh) script that runs the
                                  calibrated model (writes finalss.out,
                                  unfmt.head, and unfmt.budg)
         finalnopmp.bas          BAS1 file for no-pumping run
         finaldd.bas, finaldd.oc BAS1 and Output Control for drawdown run

      4. .\output\ directory contains model output (9 files)

         finalss.out             listing file, calibrated steady-state
                                  model (February 1993)
         finalnopmp.out          listing file, no-pumping run
         finaldd.out             listing file, drawdown run
         contour.finalss         head-contour plot file, 3 layers
         unfmt.head, unfmt.budg  binary heads and cell-by-cell budget,
                                  calibrated model (big-endian)
         unfmt.nopmp.hd,         binary heads and budget, no-pumping run
         unfmt.nopmp.budg         (big-endian)
         unfmt.dd                binary drawdown caused by February 1993
                                  pumping (big-endian)

      5. .\source\ directory contains MODFLOW source code (June 1994
         USGS version), utility source code, and run scripts (23 files)

         *.f                     Fortran source (modflow.f, bas1.f,
                                  bcf3.f, drn1.f, evt1.f, gfd1.f, ghb1.f,
                                  pcg2.f, rch1.f, riv1.f, sip1.f, sor1.f,
                                  str1.f, utl1.f, wel1.f, rmse.f, vcont.f,
                                  zonebud.f); see "Notes on rerunning
                                  the models"
         readme.text             USGS MODFLOW release notes (June 1994)
         finalss.run             UNIX shell (sh) script that runs the
                                  calibrated model (same as
                                  input\finalss.run)
         finalnopmp.run          UNIX shell (sh) script that runs the
                                  model without pumping
         finaldd.run             UNIX shell (sh) script that runs the
                                  model with February 1993 pumping and
                                  computes drawdown relative to the
                                  no-pumping heads
         compute.dd.run          UNIX shell (sh) script that runs the
                                  no-pumping and drawdown simulations and
                                  contours drawdown for the 3 layers

   D. .\wrir97-4162\ directory contains the original model archive for
      WRIR 97-4162. See contents\descriptions in this directory for the
      original file-by-file descriptions.

      README_DESCRIPTIONS OF SUBDIRECTORIES AND.docx
                                original description of subdirectories and
                                 files (Word version)

      1. .\ancillary\ directory (1 file)

         contour                 USGS contour plotting program (Data
                                  General executable; not runnable)

      2. .\contents\ directory contains original documentation (4 files)

         descriptions            descriptions of subdirectories and files
         DESCRIPTIONS OF SUBDIRECTORIES AND.docx
                                 Word version of descriptions
         instructions            instructions for running the scenarios
         reference               citation for WRIR 97-4162

      3. .\input\ directory contains MODFLOW input, run scripts, and binary
         output for the pumping scenarios (41 files)

         describes.runs          description of scenario runs and solver
                                  changes
         finalss.*               1995 model input and run script, same
                                  as .\wrir95-4049\input\ except that
                                  finalss.riv and finalss.strm do not
                                  save cell-by-cell flows (unit -30
                                  instead of 30) and finalss.sip differs
                                  only in spacing
         finaldd.oc              Output Control for drawdown run
         scen.bas, scen.oc       BAS1 and Output Control for scenarios
         scen.sip                SIP solver, 0.01-ft closure
         scen2.sip               SIP solver for scenarios 2 and 3
                                  (acceleration parameter 0.43)
         scen{1-5}.wel           Well Package for scenarios 1-5
         scencum.wel             Well Package for cumulative scenario
         scen{1-5}.run           UNIX shell (sh) scripts that run
                                  scenarios 1-5, contour drawdown for
                                  the 3 layers, and open the listing file
                                  in an editor
         scencum.run             UNIX shell (sh) script that does the
                                  same for the cumulative scenario
         unfmt.ss.head           binary heads of calibrated 1995 model,
                                  read as reference heads for drawdown
                                  (big-endian)
         unfmt.ss.hd             empty file (0 bytes) in the original
                                  archive
         unfmt.ss.budg           binary budget of calibrated 1995 model
         unfmt.head1, unfmt.headcum
                                 binary heads, scenario 1 and cumulative
         unfmt.dd{1-5}, unfmt.ddcum
                                 binary drawdown, scenarios 1-5 and
                                  cumulative (big-endian)
         unfmt.budgcum           binary budget, cumulative scenario

      4. .\output\ directory contains listing files (10 files)

         scen1.out, scencum.out  full listing files
         scen{1-5}.outf,         abbreviated listing files (heads,
         scencum.outf             drawdown, budget)
         scen1.out.001,          listing files for scenarios 1 and 4 run
         scen4.out.001            with the original 0.001-ft SIP closure

      5. .\source\ directory contains MODFLOW source code, June 1994 USGS
         version (21 files: modflow.f and package files bas1, bcf3, chd1,
         de45, drn1, evt1, gfd1, ghb1, hfb1, ibs1, pcg2, rch1, riv1, sip1,
         sor1, str1, tlk1, utl1, wel1, and readme.text)

      6. .\unpublished_scen99\ directory contains an additional pumping
         scenario that is not described in WRIR 97-4162 (6 files). The
         scenario was found in a working copy of the 1997 model files in
         the WRIR 02-4004 project directory (model97). It uses the same
         input files as the published scenarios except for the Well
         Package (20 wells, 9,555,850 ft3/d total). The source of the
         well rates is not documented. The archived run completed with a
         water-budget discrepancy of -0.12 percent. To rerun, copy these
         files into .\wrir97-4162\input\.

         scen99.run              UNIX shell (sh) script that runs the
                                  scenario and contours drawdown
         scen99.wel              Well Package
         scen99.out              listing file
         unfmt.head99            binary heads (big-endian)
         unfmt.dd99              binary drawdown (big-endian)
         unfmt.budg99            binary cell-by-cell budget (big-endian)

   E. .\wrir02-4004\ directory contains model files for WRIR 02-4004,
      selected from the project directory for that report

      1. .\ancillary\ directory contains files used to build and calibrate
         the 1999 model (2 files, 4 directories)

         gms99_original_readme.txt
                                 original 1999 description of the GMS
                                  model directories (refers to original
                                  directory names under gms99)
         original_archive_readme.muscatine
                                 original 1999 description of the WRIR
                                  02-4004 project directory (several
                                  directories listed are not included in
                                  this package)

         a. .\calibration\ directory contains calibration targets, results,
            and utilities (23 files)

            obswells.utmft       observation well locations, UTM feet
            obswellsf.{ini,map,sup}, obswellsf.{map,sup}{1-3}
                                 GMS observation coverages with
                                  calibration results (layers 1-3)
            obssum, obssum.{1-3} PostScript plots of calibration summary
            obstarg, obstarg.{1-3}
                                 PostScript plots of calibration targets
            mod99f.errsum.ps     PostScript plot of error summary
            mod99f.budget.72799  volumetric budget extracted from
                                  mod99f.out, July 27, 1999
            drain_calib.c        C utility that rewrites a Drain Package
                                  file with an elevation shift and
                                  conductance multiplier
            stream_calib.c       C utility, same purpose for the Stream
                                  Package
            strdrn               PostScript plot of stream and drain cells

         b. .\gms_conceptual_model\ directory contains GMS Map Module files
            used to generate the 200-ft model (6 files, 1 directory)

            concep99may26.{ini,map,sup}
                                 final conceptual model (sources/sinks
                                  and recharge zones; bluff recharge
                                  zones increased 2.2 percent)
            base.{ini,map,sup}   base map (roads, streams, river, drains,
                                  gravel pits)

            I.   .\mapfiles\ directory contains working and component
                 conceptual-model files (49 files)

                 concep99*.{ini,map,sup}
                                 dated working versions of the conceptual
                                  model (mar30 to may26), general-head
                                  boundaries only (concep99ghb), and
                                  porosity zones (concep99porosity,
                                  concepmpjun8)
                 gridft.{ini,map,sup}
                                 original 2,000-ft grid, rotated to UTM
                 ungen.*, ugen.* ARC/INFO ungenerate files used to build
                                  the conceptual model, UTM feet
                 mod99.allstr, mod99all.riv
                                 stream and river cells with all infilled
                                  cells

         c. .\plots\ directory contains PostScript plots of model results
            (16 files)

            99flayer1.ps, 99lflayer1.ps, 99mflayer1.ps
                                 layer 1 results, mod99f, mod99lf, mod99mf
            mod99f.lay1hd.ps, mod99f.lay2hd.ps
                                 simulated heads, layers 1 and 2
            simwt93.ps, simwtb93.ps
                                 simulated water table, February 1993
            base.ps, bound.ps, bound1.ps, mpwwells.ps
                                 base map, model boundary, municipal wells
            mod99scen.area*      PostScript plots associated with a
                                  scenario version of the model
                                  (mod99fscen, not included)

         d. .\well_data\ directory contains well data tables

            I.   .\obswells\ directory contains observation well data
                 (5 files)

                 obswells.99list  site ID, well name, latitude, longitude
                 obswells.origcov GMS coverage of 1995 observation wells
                 gpc1b.55.wls, wls.50b, wls.50b.list
                                  water levels for wells GPC1B, 50B, 55

            II.  .\supplywells\ directory contains supply well data
                 (8 files)

                 supwells.apr99   final table of supply wells: location,
                                   construction, February 1993 pumpage,
                                   and 1998 average pumpage
                 supwells.mar99, supwells.jul99
                                  earlier and later versions of the table
                 supwells.ll, supwells.prj
                                  latitude-longitude from GWSI and
                                   projection file
                 supwplgr.ll, supwplgr.pat, supwplgrft.dat
                                  GPS (PLGR) well locations, well names
                                   and February 1993 pumpage, final
                                   locations in UTM feet

      2. .\gis\ directory contains vector GIS data (ARC/INFO coverages,
         shapefiles, and map-production scripts). ARC/INFO coverages must
         be kept in their workspace directories with the workspace's info\
         directory. Coverages can be read with GDAL/OGR (AVCBin driver),
         QGIS, or ArcGIS. Figure images (TIFs), contaminant-source
         inventories, and project correspondence were not included.

         a. .\coverages\ workspace contains coverages used to construct
            the 1995 and 1999 models and to make figures for WRIR 95-4049,
            in UTM feet except where noted (53 coverages, 131 files)

            Model construction (names ending in "ft" are UTM feet copies):
              activebnd, activeft  active model boundary
              gridft, gridss       1995 model grid (gridss in UTM meters)
              mgrid1_arc, mgrid1_pol, mgrid1_pts
                                   model grid lines, cells, and nodes
              drains, drainsft     drainage ditches
              missr, missrft       Mississippi River
              slough, sloughft     Muscatine Slough
              streams, strmft      streams
              supwells, supwplgr, supwplgrft
                                   supply wells (GWSI and GPS locations)
              obswells, obswellsf, wellsf, wells077
                                   observation wells
              wlfeb93, wlaug93     water-level data, February and August
                                   1993
            Base data:
              basin, contours, iowa_out, iowa_sur, marshes, muni,
              muscbase, roads, roadsft, sects, waterbods, waterft, georef
            Other coverages (purpose not documented):
              alth, coppktgft, mseis, stdyft, stgft
            WRIR 95-4049 figure coverages:
              wri2stdy, wribnd, wribr, wrilu, wripenn, wripump, wristat,
              wristdy, wristg, wristreams, wriwater
            Other files: *.aml (ARC Macro Language map scripts), *.key
            (legend files), *.shd (shade sets), musc.{shp,shx,dbf}, ungen.*
            (ungenerate files), *.prj and project.llutmft (projection
            definitions), mgrid*.dat and muscgrid.dat (grid data),
            rowcol.lookup, obswells.ll, obswells.99list. The georef\
            subdirectory contains tic and boundary coverages for
            registering maps; it has no info\ directory and these
            coverages cannot be opened with GDAL/OGR.
            Descriptions of individual coverages above are inferred from
            coverage names and the original project notes.

         b. .\gis_figures\ workspace contains coverages and shapefiles used
            to make figures for WRIR 02-4004 (UTM meters)

            path2_poly, path5_poly, path10_poly
                                 2-, 5-, and 10-year zones of transport
            fig9.{2,5,10}_tot, fig10.{2,5,10}_tot, fig11.{2,5,10}_tot
                                 zones of transport for figures 9-11
            fig7r_tot, fig7_conts, fig7_conts2, fig7_txt, fig7.shp,
            simwt2_93            simulated water-table surface, February
                                  1993 (figure 7)
            wl_feb93             measured water levels, February 1993
            fig13_99f10, fig13_99f10r, fig13_99lf10r, fig13_99mf10r,
            fig13_99*100r.shp    10- and 100-year contributing areas for
                                  normal, less-than-normal, and greater-
                                  than-normal recharge (figures 13-14)
            ddrwdwn_lines, f1_ddlines
                                 drawdown lines
            mpw_wells.shp, other_wells.shp, supp_wells, wells, wells2,
            keiths_wells         municipal and other supply wells
            model_area, study_area, basin_bound, uplands_2
                                 model, study, and basin boundaries
            miss_riv2, creeks_2, streams2, roads_2, county_lines2,
            state_bnd2, sur_states, illowa_gne.shp, tics_cov, tics_line,
            keiths_conts3, keiths_text
                                 base data
            fig2.jpg, arcview.ps figure 2 image, PostScript plot

         c. .\musc077\ workspace contains coverages and shapefiles from the
            Muscatine Geochemistry Study (project 4619-07700, 1993-95)
            (44 files plus coverage directories)

            readme               original description (refers to a
                                  project directory not included)
            bds*, jc*, lakes, ticpts, fig{3,5,6,8,9}_{con,grd}
                                 coverages: boundary, buildings, wells,
                                  railroads, roads, contours, lakes,
                                  sections, streams, and figure contours
                                  and grids
            buildings, coal, coal2, pits, pot_wells, river, water
                                 shapefiles
            basemapgc.aml, *.key, *.ll, *.utm, *.prj
                                 map scripts, legends, location tables,
                                  projection files

      3. .\model\ directory contains the MODFLOW files for the four
         simulations described in WRIR 02-4004, one simulation per
         subdirectory. Each subdirectory is self-contained; file names
         are referenced by the GMS super file (*.mfs).

         a. .\mod99f\ 1998 average pumpage (17 files)
         b. .\mod99f93\ February 1993 pumpage (17 files)
         c. .\mod99lf\ less-than-normal recharge (16 files)
         d. .\mod99mf\ greater-than-normal recharge (16 files)

         Each subdirectory contains (shown for mod99f):

            mod99f.mfs           GMS super file: unit numbers, file names,
                                  grid origin and rotation
            mod99f.bas           Basic Package (BAS1)
            mod99f.bcf           Block-Centered Flow Package (BCF3)
            mod99f.drn           Drain Package
            mod99f.ghb           General-Head Boundary Package
            mod99f.oc            Output Control
            mod99f.rch           Recharge Package
            mod99f.riv           River Package
            mod99f.sip           Strongly Implicit Procedure solver
            mod99f.str           Stream Package (STR1)
            mod99f.wel           Well Package
            mod99f.out           listing file
            mod99f.hed           binary heads
            mod99f40.ccf         binary cell-by-cell budget
            filename.hff         MT3D flow-transport link file (named
                                  mod99f93.hff, mod99lf.hff, and
                                  mod99mf.hff in the other subdirectories)
            modflow.csh          UNIX C shell (csh) script that runs the
                                  MODFLOW executable distributed with GMS
            mod99f93.drw         (mod99f93 only) binary drawdown

         Byte order: mod99f and mod99f93 binary files are little-endian;
         mod99lf and mod99mf binary files are big-endian.

      4. .\modpath\ directory contains MODPATH version 3 files for the
         particle-tracking simulations (252 files, 3 directories). Copies
         of the MODFLOW stress files, heads (*.hed), and budgets (*40.ccf)
         used by MODPATH are included; these were rerun for MODPATH on the
         UNIX workstation and are big-endian. See README in this directory
         for the original description.

            README               original description of MODPATH files
            mod99f.*, mod99f40.ccf
                                 flow model files, 1998 pumpage
            mod99may28.*, mod99may2840.ccf
                                 flow model files, February 1993 pumpage
                                  (last GMS version of May 28, 1999)
            mod99lf.*, mod99lf40.ccf
                                 flow model files, less-than-normal
                                  recharge
            mod99mf.*, mod99mf40.ccf, od99mf.ghb
                                 flow model files, greater-than-normal
                                  recharge
            mpath99all.*         all municipal wells, 1998 pumpage
            mpath99gv.*, mpath99main.*, mpath99pp.*
                                 Grandview, Main, and Progress Park well
                                  fields, 1998 pumpage
            mpw{#}.*             individual municipal wells, 1998
                                  pumpage (#s 4, 5, 8, 9, 13, 15-20,
                                  22-36; 26 wells)
            mpath99feb93.*       all municipal wells, February 1993
                                  pumpage
            mpath99jun7.*        porosity in two zones in each of layers 1
                                  and 2
            mpath99jun7g.*       gravel-pit cell porosity = 1.0, layer 1
            mpath99jun8.*        gravel pits as zone 2; particles stop on
                                  entering pits
            mpath99lall.*, mpath99mall.*
                                 all municipal wells, less- and greater-
                                  than-normal recharge
            mp9913a.loc, mp9913c.loc
                                 alternative starting locations, MPW13
            99f.{10,100}, 99lf.{10,100}, 99mf.{10,100},
            mpwall*.ps, mpwgvpth.*.ps, mpwmnpth.*.ps, mpwpppth.*.ps
                                 PostScript plots of 2-, 5-, 10-, and
                                  100-year pathlines
            ctour1.{shp,shx,dbf,sbn,sbx}
                                 contour shapefile

            MODPATH file types:
              *.nam              MODPATH name file
              *.rsp              response file (answers to interactive
                                  prompts)
              *.mdf              main data file (porosity, IBOUND, layer
                                  elevations)
              *.loc              starting particle locations
              *.ept              endpoint file
              *.pth              pathline file
              *.sum              summary (listing) file

            a. .\ca93+all\ PostScript plots of contributing areas for
               selected wells and all wells, February 1993 and 1998 pumpage
               (7 files)
            b. .\cafields\ PostScript plots of particle endpoints for the
               Grandview, Main, and Progress Park well fields (3 files)
            c. .\cawells\ PostScript plots of contributing areas for
               individual wells MPW19, 23, 29, 31, and 35 (7 files)

REFERENCES:
----------------------------------------------------------------------------
Lucey, K.J., 1997, Evaluation of drawdown and sources of water in the
Mississippi River alluvium caused by hypothetical pumping, Muscatine, Iowa:
U.S. Geological Survey Water-Resources Investigations Report 97-4162, 18 p.,
https://doi.org/10.3133/wri974162.

Lucey, K.J., Kuzniar, R.L., and Caldwell, J.P., 1995, Hydrogeology and water
quality of the Mississippi River alluvium near Muscatine, Iowa, June 1992
through June 1994: U.S. Geological Survey Water-Resources Investigations
Report 95-4049, 74 p., https://doi.org/10.3133/wri954049.

McDonald, M.G., and Harbaugh, A.W., 1988, A modular three-dimensional
finite-difference ground-water flow model: U.S. Geological Survey
Techniques of Water-Resources Investigations, book 6, chap. A1, 586 p.,
https://doi.org/10.3133/twri06A1.

Pollock, D.W., 1994, User's guide for MODPATH/MODPATH-PLOT, version 3--A
particle tracking post-processing package for MODFLOW, the U.S. Geological
Survey finite-difference ground-water flow model: U.S. Geological Survey
Open-File Report 94-464, https://doi.org/10.3133/ofr94464.

Prudic, D.E., 1989, Documentation of a computer program to simulate
stream-aquifer relations using a modular, finite-difference, ground-water
flow model: U.S. Geological Survey Open-File Report 88-729, 113 p.,
https://doi.org/10.3133/ofr88729.

Savoca, M.E., Lucey, K.J., and Lanning, B.D., 2002, Simulation of ground-
water flow and delineation of areas contributing recharge to municipal
water-supply wells, Muscatine, Iowa: U.S. Geological Survey Water-Resources
Investigations Report 2002-4004, 26 p., https://doi.org/10.3133/wri024004.
