---
title: Molecular dynamics
layout: page
navigation: 61
author: Natasha Wood
---
# Links

# Presentations:

- [What is MD](http://aidanbudd.github.io/ppisnd/trainingMaterial/natashaWood/What_is_MD.pdf)
- [How to run MD](http://aidanbudd.github.io/ppisnd/trainingMaterial/natashaWood/How_to_run_MD.pdf)

# Software:

- [VMD](http://www.ks.uiuc.edu/Research/vmd/)
- [NAMD](http://www.ks.uiuc.edu/Research/namd/)
- [Glycam](http://glycam.org)
- [Amber/AmberTools](http://ambermd.org/)
- [RStudio](https://www.rstudio.com/products/rstudio/download/)
- [Bio3D](http://thegrantlab.org/bio3d/tutorials/installing-bio3d)

# Tutorials:

- [NAMD/VMD Tutorial](http://www.ks.uiuc.edu/Research/vmd/imd/tutorial/)
- [Chimera MD Tutorial](https://www.cgl.ucsf.edu/chimera/docs/ContributedSoftware/md/md.html)
- [Chimera Collagen Tutorial](https://www.cgl.ucsf.edu/chimera/current/docs/UsersGuide/tutorials/ensembles2.html)
- [Chimera commands for Making Animations I](https://www.cgl.ucsf.edu/chimera/data/tutorials/movies09/moviemaking.html)
- [Chimera commands for Making Animations II (older, use with caution)](http://www.cgl.ucsf.edu/chimera/data/movie-howto-mar2012/movie_examples.html#crossfade)
- [Amber Tutorial](http://ambermd.org/tutorials/advanced/tutorial8/loop1.htm)
- [Bio3D Tutorial](http://thegrantlab.org/bio3d/tutorials/structure-analysis)

# Chimera command line to animate your protein:

    movie record ; turn y 3 120 ; wait 120 ; movie stop  ; movie encode output ~/Desktop/turn.mov bitrate 10000

    movie record ; rock y 4 68 ; wait ; rock x 4 68 ; wait ; movie stop ; movie encode output ~/Desktop/rock.mov
