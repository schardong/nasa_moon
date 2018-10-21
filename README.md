# GALGOS Mission to the Moon Project

This project is an attempt to build upon NASA's provided datasets to plan a rover mission to find water on the Moon's south pole.


## Introduction

In 2009, an Indian Space Program probe found evidence of water on the Moon's south pole. Water is an important element for the establishment of longer missions, and even a permanent settlement, since it is necessary for survival, energy generation, etc.

To this date, there were several works published aiming to estimate locations where water could be found based on spectroscopy data collected from flybys. There are basically three "sources" of water for the Moon: (i) Asteroids; (ii) Solar winds; finally (iii) Moon's interior.

It has ben hypothesized that the Moon's poles may contain increased ammounts of ice water, since they are not exposed to the Sun's heat. This hypothesis is backed by Moon Mineralogy Mapper data [2].

## Our approach

### Landing site calculation

We start the planning by finding a suitable landing site for the ship. Such a landing site must obey two conditions: (i) Low slope; (ii) High probability of water near the site. The first condition is met by calculating the difference in height at every possible landing site in between parallels 75S to 90S. The second condition uses results published recently by Li *et al.* (2018), combined with data made publicly available by NASA.

We used the LOLA elevation and albedo maps [3, 4] and LAMP off and on band radio data [5] to calculate the probability of exposed ice water being present in a given region. We built upon the results of Li *et al.* (2018).

### Gauging possible routes

With the list of possible landing sites, we choose a window of operation based on a rover's estimated autonomy. The automomy is 

According to Li *et al.* (2018), we filter the map of the south pole of the Moon into Points-of-interest in which there is high probability of finding water. 

Therefore, our main application serves as a decision support for mission control planners. We have taken as a premisse that the space agencies are going to stablish a moon base 
We break this solution into two modules: (i) the selection of landing site and (ii) the space rover routing.

Firstly, the selection of landing site takes into consideration criteria such as the high incidence of Points-of-Interest within a given safety radius and a high area with a constant slope for safe landing. Therefore, we filter candidates to landing sites and score them. Then, we present the scoring of landing sites to the user for selection.

After selecting a landing site, the user may specify an amount of charges he or she wants to break the rover's exploration. The solution, then, clusters the Points-of-Interest into these points and uses an heuristic to propose a route for visiting all point in a cluster for each charging period of the space rover.


## Results

[]


## References

[1] Li, Shuai et al. **Direct evidence of surface exposed water ice in the lunar polar regions**. Proceedings of the National Academy of Sciences, v. 115, n. 36, p. 8907-8912, 2018.

[2] Moon Mineralogy Mapper, available at: https://pds-imaging.jpl.nasa.gov/volumes/m3.html

[3] LOLA GDR Digital Elevation Map, available at: http://imbrium.mit.edu/BROWSE/LOLA_GDR/POLAR/SOUTH_POLE/

[4] LOLA GDR Albedo Map, available at: http://imbrium.mit.edu/DATA/LOLA_GDR/POLAR/FLOAT_IMG/

[5] LAMP off and on band radio, available at: https://pdsimage.wr.usgs.gov/archive/lro-l-lamp-5-gdr-v1.0/LROLAM_2001/DATA/
