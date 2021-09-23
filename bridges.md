bridges
================
Duohan Zhang
9/16/2021

## github link: <https://github.com/duohan0520/my_hw_433/blob/master/faculty.html>

``` r
library(stringr)
```

    ## Warning: package 'stringr' was built under R version 4.0.2

``` r
file = readLines("Faculty.html")[166]
# I amend the original file so that Line 166 has all the info we need.
x =  strsplit(file,split=c("<br/></p></li><li><p>","<ul class=\"uw-people\"><li><p>","<br/>"))
# get a list in which each element is the info for one person.
z = strsplit(unlist(x),split = c("br"))
c(z[1],z[3764])
```

    ## [[1]]
    ## [1] "<ul class=\"uw-people\"><li><p>ABBOTT,DAVID H.<"
    ## [2] "/>Professor<"                                   
    ## [3] "/>Obstetrics &amp; Gynecology<"                 
    ## [4] "/>PHD 1979 University of Edinburgh"             
    ## 
    ## [[2]]
    ## [1] "ZWEIBEL,ELLEN G<"                 "/>Professor<"                    
    ## [3] "/>Astronomy<"                     "/>PHD 1977 Princeton University<"
    ## [5] "/></p></li></ul>"

``` r
# the info of first and last person, including some useless info.
```

``` r
str(z)
```

    ## List of 3764
    ##  $ : chr [1:4] "<ul class=\"uw-people\"><li><p>ABBOTT,DAVID H.<" "/>Professor<" "/>Obstetrics &amp; Gynecology<" "/>PHD 1979 University of Edinburgh"
    ##  $ : chr [1:4] "ABD-ELSAYED,ALAA A<" "/>Assoc Professor (Chs)<" "/>Anesthesiology<" "/>MD 2000 University of Assiut"
    ##  $ : chr [1:4] "ABDUALLAH,FAISAL<" "/>Professor<" "/>Art<" "/>PHD 2012 Royal College of Art"
    ##  $ : chr [1:4] "ABRAHAM,OLUFUNMILOLA<" "/>Assistant Professor<" "/>Pharmacy<" "/>PHD 2013 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ABRAMS,SAMANTHA<" "/>Assoc Lecturer<" "/>Information School<" "/>MA 2017 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ABRAMSON,LYN<" "/>Professor<" "/>Psychology<" "/>PHD 1978 University of Pennsylvania"
    ##  $ : chr [1:4] "ACKER,LINDSAY<" "/>Lecturer<" "/>Accting &amp; Info Sys<" "/>MACC 2005 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ACKERMAN,STEVEN<" "/>Professor<" "/>Atmospheric &amp; Oceanic Sciences<" "/>PHD 1987 Colorado State University"
    ##  $ : chr [1:4] "ADAMCZYK,PETER GABRIEL<" "/>Assistant Professor<" "/>Mechanical Engineering<" "/>PHD 2008 Univ of Michigan at Ann Arbor"
    ##  $ : chr [1:4] "ADAMES-CORRALIZA,ANGEL<" "/>Assistant Professor<" "/>Atmospheric &amp; Oceanic Sciences<" "/>PHD 2018 University of Washington"
    ##  $ : chr [1:4] "ADAMS,AERON<" "/>Clinical Asst Prof<" "/>Nursing<" "/>DNP 2017 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ADAMS,MEGAN<" "/>Asst Faculty Assoc<" "/>Information School<" "/>MA  University of South Florida"
    ##  $ : chr [1:4] "ADCOCK,SARAH<" "/>Assistant Professor<" "/>Animal And Dairy Sciences<" "/>PHD 2020 Univ of California Davis"
    ##  $ : chr [1:4] "ADDINGTON,REBECCA LYNN<" "/>Senior Lecturer<" "/>Psychology<" "/>PHD 1998 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ADDO,FENABA<" "/>Associate Professor<" "/>School Of Human Ecology<" "/>PHD 2012 Ithaca College"
    ##  $ : chr [1:4] "ADELL,SANDRA<" "/>Professor<" "/>Afro-American Studies<" "/>PHD 1989 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "AFFI,ABOUD<" "/>Clinical Adjunct Professor<" "/>Volunteer Staff<" "/>MD 1989 University Of Aleppo"
    ##  $ : chr [1:4] "AGARWAL,PRIYANKA<" "/>Assistant Professor<" "/>Curriculum And Instruction<" "/>PHD 2019 Univ of California Irvine"
    ##  $ : chr [1:4] "AGASIE,ROBERT<" "/>Instrmt Innovator/Ins<" "/>Engineering Research Center<" "/>MS 1997 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "AGOKE,ADEOLA<" "/>Asst Faculty Assoc<" "/>African Cultural Studies<" "/>PHD 2019 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "AHLQUIST,PAUL GERALD<" "/>Professor<" "/>Plant Pathology<" "/>PHD 1981 Univ of Wisconsin-Madison"
    ##  $ : chr [1:3] "AHMAD,JAMEEL<" "/>Senior Lecturer<" "/>South Asian Sum Lang Instit"
    ##  $ : chr [1:4] "AHMAD,NIHAL<" "/>Professor<" "/>Dermatology<" "/>PHD 1989 University of Lucknow"
    ##  $ : chr [1:4] "AHMED,AZAM SYED<" "/>Assoc Professor (Chs)<" "/>Neurological Surgery<" "/>MD 2003 Loyola University of Chicago"
    ##  $ : chr [1:4] "AHN,JAERIN<" "/>Assoc Faculty Assoc<" "/>Asian Languages &amp; Cultures<" "/>MA 2013 Ewha Womans University"
    ##  $ : chr [1:4] "AHN,SUE<" "/>Professor<" "/>Civil &amp; Environmental Engr<" "/>PHD  Univ of California Berkeley"
    ##  $ : chr [1:4] "AHN,YEOHYUN<" "/>Assistant Professor<" "/>Art<" "/>MFA 2007 Maryland Institute Colg Of Art"
    ##  $ : chr [1:4] "AHRENS,SARAH ELIZABETH<" "/>Clinical Assoc Prof<" "/>Medicine<" "/>MD 2002 U of California San Francisco"
    ##  $ : chr [1:4] "AI,ALBERT L<" "/>Visiting Asst Prof<" "/>Mathematics<" "/>PHD 2019 Univ of California Berkeley"
    ##  $ : chr [1:4] "AIKEN,JEFFREY P<" "/>Adjunct Instructor<" "/>Law School<" "/>JD 1972 Marquette University"
    ##  $ : chr [1:4] "AIZAWA,NAOKI<" "/>Assistant Professor<" "/>Economics<" "/>PHD 2014 University of Pennsylvania"
    ##  $ : chr [1:4] "AJMANI,VIVEK<" "/>Assoc Faculty Assoc<" "/>Engr Professional Development<" "/>PHD  "
    ##  $ : chr [1:4] "AKELLA,ADITYA<" "/>Professor<" "/>Computer Sciences<" "/>PHD 2005 Carnegie-Mellon University"
    ##  $ : chr [1:4] "AL-ADRA,DAVID<" "/>Assistant Professor<" "/>Surgery<" "/>PHD 2012 University of Alberta"
    ##  $ : chr [1:4] "AL-SUBU,AWNI M<" "/>Asst Professor (Chs)<" "/>Pediatrics<" "/>MD 2005 Al-Quds University"
    ##  $ : chr [1:4] "ALAGOZ,OGUZHAN<" "/>Professor<" "/>Industrial &amp; Systems Engr<" "/>PHD 2004 University of Pittsburgh"
    ##  $ : chr [1:4] "ALARID,ELAINE<" "/>Professor<" "/>Oncology<" "/>PHD 1991 Univ of California Berkeley"
    ##  $ : chr [1:4] "ALATOUT,SAMER N<" "/>Associate Professor<" "/>Community &amp; Environ Sociology<" "/>PHD 2002 Cornell University"
    ##  $ : chr [1:4] "ALBARGHOUTHI,AWS<" "/>Assistant Professor<" "/>Computer Sciences<" "/>PHD 2014 University of Toronto"
    ##  $ : chr [1:4] "ALBERS,CRAIG<" "/>Associate Professor<" "/>Educational Psychology<" "/>PHD 2002 Arizona State University"
    ##  $ : chr [1:4] "ALBERT,LAURA<" "/>Professor<" "/>Industrial &amp; Systems Engr<" "/>PHD 2006 Univ of IL at Urbana-Champaign"
    ##  $ : chr [1:4] "ALBERTINI,MARK RICHARD<" "/>Professor<" "/>Medicine<" "/>MD 1984 University of Vermont"
    ##  $ : chr [1:4] "ALCALA GALAN,MERCEDES<" "/>Associate Professor<" "/>Spanish And Portuguese<" "/>PHD 1994 Univ Complutense de Madrid"
    ##  $ : chr [1:4] "ALDAG,RAY<" "/>Professor<" "/>Management &amp; Human Resources<" "/>PHD 1974 Michigan State University"
    ##  $ : chr [1:4] "ALDER,SIMEON DAVID<" "/>Faculty Associate<" "/>Economics<" "/>PHD 2009 Univ of California Los Angeles"
    ##  $ : chr [1:3] "ALESSANDRINO,KAYLA<" "/>Clinical Instructor<" "/>Medical Sciences"
    ##  $ : chr [1:4] "ALEXANDER,ANDREW LAFAYETTE<" "/>Professor<" "/>Medical Physics<" "/>PHD 1994 University of Arizona"
    ##  $ : chr [1:4] "ALEXANDER,ANGELA<" "/>Faculty Associate<" "/>English<" "/>MA 2007 University Of Central Florida"
    ##  $ : chr [1:4] "ALEXANDER,LACEY ANN<" "/>Clinical Asst Prof<" "/>Nursing<" "/>PHD 2018 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ALI,SHANTEL D<" "/>Asst Prof Of Mil Sci<" "/>Military Science<" "/>BA 2002 "
    ##  $ : chr [1:4] "ALI,SYED EKHTEYAR<" "/>Senior Lecturer<" "/>South Asian Sum Lang Instit<" "/>PHD  "
    ##  $ : chr [1:4] "ALIBALI,MARTHA W.<" "/>Professor<" "/>Psychology<" "/>PHD 1994 University of Chicago"
    ##  $ : chr [1:4] "ALISCH,REID S<" "/>Assistant Professor<" "/>Neurological Surgery<" "/>PHD 2003 Univ of Michigan at Ann Arbor"
    ##  $ : chr [1:4] "ALLEN,CAITILYN<" "/>Professor<" "/>Plant Pathology<" "/>PHD 1987 VA Polytechnic Inst &amp; State U"
    ##  $ : chr [1:4] "ALLEN,DAVID<" "/>Professor<" "/>Pediatrics<" "/>MD 1980 Duke University"
    ##  $ : chr [1:4] "ALLEN,HEATHER<" "/>Associate Professor<" "/>French And Italian<" "/>PHD 2002 Emory University"
    ##  $ : chr [1:4] "ALLEN,MATT<" "/>Professor<" "/>Engineering Physics<" "/>PHD 2005 Georgia Inst of Technology"
    ##  $ : chr [1:4] "ALLEWAERT,MONIQUE<" "/>Associate Professor<" "/>English<" "/>PHD 2006 Duke University"
    ##  $ : chr [1:4] "ALLIE,MARK C<" "/>Faculty Associate<" "/>Electrical &amp; Computer Engr<" "/>MS 1983 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ALONSO,ARACELI<" "/>Dis Lecturer<" "/>Gender And Women Studies<" "/>PHD 2002 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ALTINO,SOH-HYUN PARK<" "/>Associate Professor<" "/>Mead Witter School Of Music<" "/>PHD 2002 Cleveland Institute Of Music"
    ##  $ : chr [1:4] "ALTSCHAFL,BETH<" "/>Faculty Associate<" "/>Academic Affairs<" "/>PHD 2006 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ALTSECH,MOSES<" "/>Lecturer<" "/>Marketing<" "/>PHD 1996 Pennsylvania State University"
    ##  $ : chr [1:4] "ALTWIES,JOY<" "/>Faculty Associate<" "/>Engr Professional Development<" "/>PHD 2013 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ALVAREZ,ELIZABETH E<" "/>Clinical Asst Prof<" "/>Medical Sciences<" "/>DVM 2003 Michigan State University"
    ##  $ : chr [1:4] "ALVAREZ,SAYLIN<" "/>Senior Lecturer<" "/>Spanish And Portuguese<" "/>PHD  Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "AMADOR-NOGUEZ,DANIEL<" "/>Associate Professor<" "/>Bacteriology<" "/>PHD 2007 Baylor University"
    ##  $ : chr [1:4] "AMANN,KURT<" "/>Associate Professor<" "/>Integrative Biology<" "/>PHD 1999 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "AMASINO,RICHARD M.<" "/>Professor<" "/>Biochemistry<" "/>PHD 1982 Indiana University"
    ##  $ : chr [1:4] "AMATO,FELICE CATHERINE<" "/>Lecturer<" "/>Art<" "/>PHD 2018 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "AMINE,LAILA<" "/>Associate Professor<" "/>English<" "/>PHD 2011 Indiana University"
    ##  $ : chr [1:4] "AMSBARY,PAUL<" "/>Adjunct Assoc Prof<" "/>Information School<" "/>MS 2007 Georgia Inst of Technology"
    ##  $ : chr [1:4] "AN,PANDUAN<" "/>Visiting Asst Prof<" "/>Statistics<" "/>PHD 2019 Ohio University"
    ##  $ : chr [1:4] "AN,ZHE GIGI<" "/>Assistant Professor<" "/>Rehab Psychology &amp; Special Ed<" "/>PHD 2018 University of Kansas"
    ##  $ : chr [1:4] "ANANTHARAMAN,KARTHIK<" "/>Assistant Professor<" "/>Bacteriology<" "/>PHD 2014 Univ of Michigan at Ann Arbor"
    ##  $ : chr [1:4] "ANCOS GARCIA,PABLO<" "/>Associate Professor<" "/>Spanish And Portuguese<" "/>PHD 2004 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ANDERSEN,CLAUS E<" "/>Assistant Professor<" "/>German, Nordic &amp; Slavic<" "/>PHD 2015 University of Helsinki"
    ##  $ : chr [1:4] "ANDERSON,DAVID<" "/>Professor<" "/>Electrical &amp; Computer Engr<" "/>PHD 1984 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ANDERSON,DAVID F<" "/>Professor<" "/>Mathematics<" "/>PHD 2005 Duke University"
    ##  $ : chr [1:4] "ANDERSON,KATHRYN<" "/>Lecturer<" "/>Community &amp; Environ Sociology<" "/>PHD 2019 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ANDERSON,LORI<" "/>Assistant Professor<" "/>Nursing<" "/>PHD 2006 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ANDERSON,MARK<" "/>Assistant Professor<" "/>Mechanical Engineering<" "/>PHD 1998 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ANDERSON,PETER<" "/>Senior Lecturer<" "/>Nutritional Sciences<" "/>MS 1995 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ANDERSON,RICHARD A.<" "/>Professor<" "/>Administration<" "/>PHD 1982 Univ of Minnesota-Twin Cities"
    ##  $ : chr [1:4] "ANDERSON,ROZALYN<" "/>Associate Professor<" "/>Medicine<" "/>PHD 1999 Univ of Dublin-Trinity College"
    ##  $ : chr [1:4] "ANDES,DAVID R.<" "/>Professor<" "/>Medicine<" "/>MD 1992 Univ of Missouri-Columbia"
    ##  $ : chr [1:4] "ANDREAE,SUSAN J<" "/>Assistant Professor<" "/>Kinesiology<" "/>PHD 2015 Univ of Alabama at Birmingham"
    ##  $ : chr [1:4] "ANDRESEN,CHRISTIAN G.<" "/>Assistant Professor<" "/>Geography<" "/>PHD 2014 University Of Texas At El Paso"
    ##  $ : chr [1:4] "ANDREWS,JOSEPH<" "/>Assistant Professor<" "/>Mechanical Engineering<" "/>PHD 2019 Duke University"
    ##  $ : chr [1:4] "ANDREWS,LISA M<" "/>Assoc Faculty Assoc<" "/>Consumer Science<" "/>MBA 2004 Univ of Wisconsin-Madison"
    ##  $ : chr [1:4] "ANDREWS,URI<" "/>Associate Professor<" "/>Mathematics<" "/>PHD 2010 Univ of California Berkeley"
    ##  $ : chr [1:4] "ANDRZEJEWSKI,ANNA<" "/>Professor<" "/>Art History<" "/>PHD 2001 University of Delaware"
    ##  $ : chr [1:4] "ANE,CECILE<" "/>Professor<" "/>Botany<" "/>PHD 2000 U de Toulouse II (Le Mirail)"
    ##  $ : chr [1:4] "ANE,JEAN-MICHEL<" "/>Professor<" "/>Bacteriology<" "/>PHD 2002 U de Toulouse II (Le Mirail)"
    ##  $ : chr [1:4] "ANEX,ROBERT<" "/>Professor<" "/>Biological Systems Engineering<" "/>PHD 1995 Univ of California Davis"
    ##  $ : chr [1:4] "ANGENENT,SIGURD B.<" "/>Professor<" "/>Mathematics<" "/>PHD 1986 State Univ Of Leiden"
    ##  $ : chr [1:4] "ANGULO BRACHO,HERNAN LIZARDO<" "/>Clinical Instructor<" "/>Medical Sciences<" "/>DVM 1999 Univ Ncnl Autonoma de Mexico"
    ##  $ : chr [1:4] "ANGUS,JENNIFER<" "/>Professor<" "/>School Of Human Ecology<" "/>MFA 1991 Sch Of The Art Inst Of Chicago"
    ##  $ : chr [1:4] "ANIBAS,CALLI<" "/>Assoc Research Spec<" "/>Agronomy<" "/>MS 2020 Univ of Wisconsin-Madison"
    ##   [list output truncated]
