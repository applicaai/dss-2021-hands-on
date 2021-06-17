
Intro
-----

Getting GEval evaluation tool (should work on 64-bit Linuxes)

    wget https://gonito.net/get/bin/geval
    chmod u+x geval
    ./geval --version

Cloning a challenge with a sample solution

    git clone --single-branch git://gonito.net/twitter-sentiment-analysis -b submission-04376
    cd twitter-sentiment-analysis

Evaluating the solution

    ../geval -t dev-0

Show the first items evaluated

    ../geval -t dev-0 --line-by-line | head -n 5

Show me the worst 5 items

    ../geval -t dev-0 --line-by-line -s | head -n 5

Show me the features which worsen the results a lot

    ../geval -t dev-0 -w | head -n 20

What's wrong with "Lol"?

    ../geval -t dev-0 --line-by-line --filter 'in<1>:lol' | shuf -n 2

Puzzle — what's wrong in this output of a Machine Translation system?

    cd ..
    git clone git://gonito.net/wmt-2017 -b submission-01229 --single-branch

Kleister information extraction challenges
------------------------------------------

    git clone https://github.com/applicaai/kleister-nda
    cd kleister-nda
    cat dev-0/expected.tsv | head -n 1

    cd ..
    git clone https://github.com/applicaai/kleister-charity
    cd kleister-charity
    cat dev-0/expected.tsv | head -n 1
