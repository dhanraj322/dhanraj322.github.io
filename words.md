layout: page
title: "words"
permalink: /words
<html>
<head>
    <title>Search Links - Groups</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            font-family: Arial, sans-serif;
        }
        h1 {
            margin-bottom: 20px;
        }
        h2 {
            margin-top: 40px;
        }
        ul {
            padding: 0;
        }
        li {
            margin-bottom: 10px;
            font-size: 18px;
            list-style-type: none;
        }
        a {
            color: #007bff;
            text-decoration: none;
        }
    </style>
</head>
<body>

<div id="content"></div>

<script>
    function createGroup(groupNumber, words) {
        var content = document.getElementById('content');
        var groupDiv = document.createElement('div');
        groupDiv.innerHTML = '<h2>------------------------------------ ' + groupNumber + ' ------------------------------------</h2><ul>';
        
        for (var i = 0; i < words.length; i++) {
            var word = words[i];
            var googleSearchLink = 'https://www.google.com/search?q=' + word;
            var someLink = 'https://mnemonicdictionary.com/?word=' + word;
            groupDiv.innerHTML += '<li><a href="' + googleSearchLink + '">' + word + '</a> &nbsp; <a href="' + someLink + '">' + word + '</a></li>';
        }
        
        groupDiv.innerHTML += '</ul>';
        content.appendChild(groupDiv);
    }

    // Define the list of groups and their corresponding words
    var groups = [
        [
            "abound", "amorphous", "austere", "belie", "capricious", "cerebral", "congenial", "conspicuous", "cursory", "daunting",
            "deify", "didactic", "disseminate", "feasible", "flout", "homogeneous", "humdrum", "insipid", "loquacious", "misanthropic",
            "misnomer", "negligent", "obsequious", "placate", "proclivity", "puerile", "quixotic", "spendthrift", "taciturn", "wary"
        ],
        [
            "adulterate", "advocate", "aggrandize", "alacrity", "ambivalent", "ameliorate", "amenable", "anachronistic", "audacious", "avaricious",
            "banal", "benign", "brazen", "calumny", "candid", "castigate", "caustic", "construe", "contrite", "convoluted",
            "covet", "craven", "decorum", "deft", "demur", "derivative", "desiccate", "diatribe", "incredulous", "ingenuous"
        ],
        [
            "abate", "abjure", "anomalous", "antipathy", "arcane", "arduous", "artless", "ascetic", "assuage", "betray",
            "bucolic", "burgeon", "cacophonous", "canonize", "censure", "chicanery", "coalesce", "cogent", "compelling", "contend",
            "copious", "cosmopolitan", "deference", "desultory", "diffident", "dilatory", "equivocate", "polarize", "prodigal", "verbose"
        ],
        [
            "abstain", "approbation", "cherish", "corroborate", "disparate", "emulate", "enervate", "ephemeral", "fervid", "garrulous",
            "incendiary", "inimical", "intimate", "invigorate", "mitigate", "obsolete", "opaque", "paradigmatic", "pedantic", "placid",
            "polemical", "precipitate", "profundity", "prophetic", "prudent", "punctilious", "recondite", "scrupulous", "tranquil", "vacillate"
        ],
        [
            "aloof", "clangor", "conventional", "debunk", "diminutive", "discernible", "enigmatic", "estranged", "extravagant", "fanciful",
            "frivolous", "heterogeneous", "imperious", "impertinent", "invasive", "irresolute", "laudable", "lax", "marginalize", "panache",
            "plodding", "prosaic", "remedial", "restive", "sporadic", "stigmatize", "undermine", "utterly", "weary", "zealous"
        ],


        // 6
        [
            "admonish", "aesthetic", "affectation", "alleviate", "analogous", "bolster", "chauvinistic", "connoisseur", "dissemble",
            "dogged", "dupe", "empirical", "engender", "entitled", "pertinacious", "presumptuous", "probity", "proliferate",
            "specious", "spurious", "subjective", "subvert", "timorous", "tortuous", "tractable", "transient", "ubiquitous",
            "underscore", "venal", "venerate"
        ],
        [
            "appease", "arbitrary", "archaic", "clamorous", "dearth", "explicable", "hyperbole", "immutable", "indefatigable",
            "indolent", "insular", "intransigent", "intrepid", "irreverent", "loathe", "malign", "malleable", "neophyte",
            "plastic", "platitude", "prescient", "pristine", "reproach", "robust", "salubrious", "sanction", "sedulous",
            "soporific", "stern", "tendentious"
        ],
        [
            "accentuate", "conjectural", "convivial", "decadent", "egregious", "evanescent", "flamboyant", "forestall", "gainsay",
            "galvanize", "indiscriminate", "innocuous", "momentary", "mundane", "nettlesome", "nullify", "obviate", "omnipresent",
            "oust", "palpable", "perfidy", "profuse", "pugnacious", "sagacious", "sanguine", "scant", "skullduggery", "trivial",
            "utilitarian", "vapid"
        ],
        [
            "boorish", "brook", "circumspect", "comity", "commensurate", "cordial", "deleterious", "dichotomy", "edify", "elicit",
            "erudite", "fecund", "feeble", "felicitous", "forbear", "haphazard", "hodgepodge", "impede", "impetuous", "irascible",
            "mercenary", "meticulous", "mordant", "outstrip", "precarious", "quirky", "repudiate", "tact", "trifling", "turbulent"
        ],
        [
            "acumen", "antithesis", "ascribe", "befuddled", "eschew", "esoteric", "evasive", "exculpate", "expedite", "fastidious",
            "feign", "furtive", "hamper", "indispensable", "lament", "myopic", "nonchalant", "partial", "pensive", "portend",
            "provincial", "rudimentary", "salutary", "sever", "slight", "somnolent", "stoic", "supersede", "tout", "wane"
        ],


        // 11
        [
            "abhor", "boisterous", "chivalrous", "churlish", "clandestine", "complacent", "cumbersome", "debilitating", "deliberate",
            "droll", "eccentric", "fractious", "limpid", "mawkish", "obeisance", "ostentatious", "panacea", "perfunctory", "perilous",
            "pervasive", "preclude", "predilection", "rapacious", "relish", "satirical", "sham", "skirt", "sluggish", "spartan", "truculent"
        ],
        [
            "acrimonious", "belligerent", "beneficent", "canny", "cavalier", "distressed", "dwindling", "eclipse", "encyclopedic",
            "exacerbate", "exasperated", "fungible", "hackneyed", "incongruous", "interchangeable", "laconic", "lucrative",
            "magisterial", "onerous", "opprobrium", "parsimonious", "peripheral", "provocative", "renounce", "tempestuous",
            "tenable", "transgression", "urbane", "verisimilitude", "vitiate"
        ],
        [
            "affinity", "altruistic", "baroque", "byzantine", "compromise", "conciliatory", "countenance", "covert", "credible",
            "diffuse", "documentary", "exhaustive", "exhilarating", "extraneous", "fervor", "futile", "illusory", "invidious",
            "lethargic", "metaphorical", "mimic", "numinous", "obscure", "overt", "pellucid", "perpetuate", "rational",
            "scathing", "subtle", "superficial"
        ],
        [
            "acquiesce", "adroit", "amend", "animus", "apologist", "astringent", "collaborate", "competent", "correlate",
            "deride", "dictate", "discreet", "divorced", "elitist", "exacting", "flummoxed", "fruitful", "inborn", "polymath",
            "reticent", "stringent", "subservient", "surreptitious", "tantalizing", "tantamount", "torpor", "trenchant", "umbrage",
            "versatile", "wayward"
        ],
        [
            "alienate", "apathy", "apropos", "apt", "cloak", "consensus", "distort", "divergent", "elated", "enchant",
            "entrenched", "exotic", "exploitative", "foreseeable", "forsake", "gratify", "heed", "judicious", "lucid",
            "pertinent", "propriety", "scintillating", "sensational", "sophisticated", "strife", "understated", "unscrupulous",
            "veracity", "virulent", "volatile"
        ],

        // 16
        [
            "antedate", "banish", "bridle", "comply", "crestfallen", "curtail", "elucidate", "evade", "feckless", "fester",
            "iconoclastic", "immure", "improvise", "inhibit", "inscrutable", "lionize", "monotonous", "peculiar", "premeditate",
            "profligate", "reconcile", "refine", "relinquish", "ruminate", "skittish", "superfluous", "synoptic", "thorough",
            "visionary", "vociferous"
        ],
        [
            "acclaim", "ascertain", "assertive", "bogus", "cataclysmic", "circumscribe", "complementary", "contentious",
            "disingenuous", "divulge", "dogmatic", "fallacious", "foolhardy", "hinder", "impair", "impugn", "incessant",
            "inclined", "inveterate", "miserly", "patent", "petulant", "pithy", "pliant", "sanctimonious", "sound", "tarnish",
            "tepid", "upbraid", "vexation"
        ],
        [
            "abet", "accessible", "acquisitive", "amalgamate", "attenuate", "augment", "aversion", "blithe", "contempt",
            "dawdle", "deflect", "discount", "dissident", "efficacious", "equitable", "erratic", "industrious", "inform",
            "irksome", "manacle", "modest", "noxious", "pernicious", "predicament", "proficient", "prolix", "scorn",
            "subordinate", "unseemly", "veritable"
        ],
        [
            "acolyte", "anoint", "base", "coercion", "coin", "cunning", "discomfit", "dissent", "distill", "dubious",
            "ebullient", "facetious", "fallible", "florid", "gawky", "inveigle", "jettison", "mendacity", "munificent",
            "naive", "noble", "parochial", "pedestrian", "prevaricate", "prime", "radical", "recrudescent", "temporal",
            "transitory", "viable"
        ],
        [
            "abreast", "confound", "digression", "discrepancy", "duplicitous", "expedient", "fabricate", "glum", "harbinger",
            "intrinsic", "largesse", "libertine", "malfeasance", "manifest", "minute", "modish", "nascent", "perennial", "pious",
            "providential", "prowess", "schism", "slander", "stalwart", "supplicate", "terse", "tirade", "universal", "vanquish", "woeful"
        ],

        // 21
        [
            "abject", "amicable", "animosity", "aver", "barrage", "cathartic", "decipher", "delusion", "dispense", "eloquent",
            "enthrall", "eradicate", "fledgling", "fortitude", "fortuitous", "goad", "imminent", "incontrovertible", "itinerant",
            "magnanimous", "meritorious", "mutiny", "paradoxical", "perseverance", "render", "repertoire", "resilient", "resolute",
            "supple", "valor"
        ],
        [
            "arresting", "chastise", "cumbersome", "economy", "elementary", "embellish", "euphoric", "exonerate", "extrapolate",
            "falter", "fervent", "foment", "gaffe", "heterodox", "histrionic", "implicit", "inviolate", "liability", "obstinate",
            "painstaking", "phlegmatic", "prodigious", "propensity", "qualm", "renege", "stinting", "temper", "tentative", 
            "unprecedented", "vivacious"
        ],
        [
            "allusive", "astute", "commence", "convalescent", "curb", "decry", "duress", "evoke", "fawn", "fret", "glib", 
            "headstrong", "intermittent", "ire", "languid", "lull", "mettlesome", "mollify", "neutralize", "nonplussed", 
            "precipitous", "pretentious", "profound", "propagate", "recourse", "refute", "regress", "repercussion", 
            "replenish", "vigilant"
        ],
        [
            "assail", "benevolent", "berate", "buoyant", "buttress", "condone", "contravene", "denounce", "despotic", 
            "deviate", "disinterested", "escalate", "exorcise", "finicky", "foil", "intertwined", "inundate", "ironclad", 
            "jeopardize", "mercurial", "oblivious", "perpetrate", "plaintive", "poignant", "quiescent", "reiterate", 
            "subside", "subsume", "surmount", "tangential"
        ],
        [
            "adept", "adverse", "appropriate", "archetype", "articulate", "auspicious", "bereft", "captious", "conclusive",
            "conspire", "delineate", "disentangle", "exhort", "frailty", "grievance", "harangue", "ploy", "poise", "pomposity",
            "proxy", "relent", "rhetoric", "rigor", "sparse", "steadfast", "suspect", "tedious", "vitality", "whimsical", "yield"
        ],

        // 26
        [
            "apprehension", "ardent", "axiomatic", "cease", "conducive", "corporeal", "doctrinaire", "eclectic", "equanimity",
            "exorbitant", "fickle", "figurative", "flustered", "gullible", "idiosyncratic", "incidental", "ingrained", "insolent",
            "lampoon", "lavish", "lugubrious", "macabre", "morose", "officious", "ramification", "serene", "supplant", "tacit",
            "transcend", "treatise"
        ],
        [
            "antagonize", "barren", "bombastic", "cajole", "chary", "curmudgeon", "dirge", "estimable", "euphemism",
            "excoriate", "exigent", "haughty", "heady", "imperturbable", "implacable", "lambaste", "miscreant",
            "peccadillo", "philistine", "relegate", "repugnant", "sentimental", "squander", "swindle", "tangible",
            "turpitude", "unalloyed", "undercut", "wheedle", "xenophobic"
        ],
        [
            "abeyance", "abstract", "affront", "agitate", "august", "burnish", "coy", "deprecate", "disdain",
            "disperse", "distend", "endemic", "enmity", "gauche", "hysterical", "impudent", "inchoate", "penchant",
            "quandary", "quarantine", "quash", "quibble", "ravage", "recant", "redoubtable", "retiring", "shrill",
            "sophistry", "substantiate", "wily"
        ],
        [
            "abscond", "apogee", "aspersion", "bawdy", "chagrin", "collude", "commiserate", "conflagration",
            "contretemps", "conviction", "croon", "depose", "detente", "dowdy", "echelon", "ennui", "expatiate",
            "fraught", "fulcrum", "imbroglio", "jocund", "languish", "nadir", "nimble", "ominous", "outlandish",
            "propitious", "prurient", "sadistic", "zenith"
        ],
        [
            "aberrant", "abide", "bravado", "callow", "capitulate", "cogitate", "deportment", "extemporize",
            "factious", "fallow", "feint", "flagrant", "gratuitous", "grovel", "indecorous", "intrigue", "nominal",
            "obdurate", "obstreperous", "odious", "plucky", "precocious", "remuneration", "slovenly", "soliloquy",
            "spurn", "stolid", "temerity", "tenuous", "verve"
        ],

        // 31
        [
            "abrogate", "aghast", "apprise", "beguile", "boon", "callous", "coddle", "crescendo",
            "extenuating", "frenetic", "fringe", "hapless", "immaculate", "obfuscate", "ossify", "pastiche",
            "perspicacious", "ponderous", "recluse", "retaliate", "rhapsody", "serendipitous", "shirk", "sinecure",
            "sinuous", "sordid", "stanch", "surfeit", "ulterior", "voluble"
        ],
        [
            "abstruse", "auxiliary", "caricature", "depravity", "dilettante", "effrontery", "encroach", "endow",
            "entreat", "gregarious", "indictment", "indignant", "ineluctable", "inquisitive", "latitude", "levity",
            "malevolent", "mediate", "occlude", "pacify", "paragon", "patronize", "penurious", "piquant", "rampant",
            "remote", "reprobate", "turbid", "turgid", "vacuous"
        ]
    ];

    // Loop through the groups and create the content
    for (var i = 0; i < groups.length; i++) {
        var groupNumber = i + 1;
        var words = groups[i];
        createGroup(groupNumber, words);
    }
</script>

</body>
</html>
