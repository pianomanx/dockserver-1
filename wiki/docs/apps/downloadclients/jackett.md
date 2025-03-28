      
<p align="left">
    <a href="https://discord.gg/FYSvu83caM">
        <img src="https://discord.com/api/guilds/830478558995415100/widget.png?label=Discord%20Server&logo=discord" alt="Join DockServer on Discord">
    </a>
        <a href="https://github.com/dockserver/dockserver/releases">
        <img src="https://img.shields.io/github/downloads/dockserver/dockserver/total?label=Total%20Downloads&logo=github" alt="Total Releases Downloaded from GitHub">
    </a>
    <a href="https://github.com/dockserver/dockserver/releases/latest">
        <img src="https://img.shields.io/github/v/release/dockserver/dockserver?include_prereleases&label=Latest%20Release&logo=github" alt="Latest Official Release on GitHub">
    </a>
    <a href="https://github.com/dockserver/dockserver/blob/master/LICENSE">
        <img src="https://img.shields.io/github/license/dockserver/dockserver?label=License&logo=gnu" alt="GNU General Public License">
    </a>
</p>

# Jackett

[![GitHub issues](https://img.shields.io/github/issues/Jackett/Jackett.svg?maxAge=60&style=flat-square)](https://github.com/Jackett/Jackett/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/Jackett/Jackett.svg?maxAge=60&style=flat-square)](https://github.com/Jackett/Jackett/pulls)
[![Build Status](https://dev.azure.com/Jackett/Jackett/_apis/build/status/Jackett.Jackett?branchName=master)](https://dev.azure.com/jackett/jackett/_build/latest?definitionId=1&branchName=master)
[![GitHub Releases](https://img.shields.io/github/downloads/Jackett/Jackett/total.svg?maxAge=60&style=flat-square)](https://github.com/Jackett/Jackett/releases/latest)
[![Docker Pulls](https://img.shields.io/docker/pulls/linuxserver/jackett.svg?maxAge=60&style=flat-square)](https://hub.docker.com/r/linuxserver/jackett/)
[![Discord](https://img.shields.io/badge/discord-chat-7289DA.svg?maxAge=60&style=flat-square)](https://discord.gg/J865QuA)

This project is a new fork and is recruiting development help.  If you are able to help out please [contact us](https://github.com/Jackett/Jackett/issues/8180).

Please see our [troubleshooting and contributing guidelines](CONTRIBUTING.md) before submitting any issues or pull requests

Jackett works as a proxy server: it translates queries from apps ([Sonarr](https://github.com/Sonarr/Sonarr), [Radarr](https://github.com/Radarr/Radarr), [SickRage](https://sickrage.github.io/), [CouchPotato](https://couchpota.to/), [Mylar](https://github.com/evilhero/mylar), [Lidarr](https://github.com/lidarr/lidarr), [DuckieTV](https://github.com/SchizoDuckie/DuckieTV), [qBittorrent](https://www.qbittorrent.org/), [Nefarious](https://github.com/lardbit/nefarious) etc.) into tracker-site-specific http queries, parses the html response, then sends results back to the requesting software. This allows for getting recent uploads (like RSS) and performing searches. Jackett is a single repository of maintained indexer scraping & translation logic - removing the burden from other apps.

Developer note: The software implements the [Torznab](https://github.com/Sonarr/Sonarr/wiki/Implementing-a-Torznab-indexer) (with hybrid [nZEDb](https://github.com/nZEDb/nZEDb/blob/b485fa326a0ff1f47ce144164eb1f070e406b555/resources/db/schema/data/10-categories.tsv)/[Newznab](https://newznab.readthedocs.io/en/latest/misc/api/#predefined-categories) [category numbering](https://github.com/Jackett/Jackett/wiki/Jackett-Categories)) and [TorrentPotato](https://github.com/RuudBurger/CouchPotatoServer/wiki/Couchpotato-torrent-provider) APIs.

A third-party Golang SDK for Jackett is available from [webtor-io/go-jackett](https://github.com/webtor-io/go-jackett)

<details> <summary> <b> Supported Public Trackers </b> </summary>

 * 1337x
 * 7torrents
 * ACG.RIP
 * ACGsou (36DM)
 * Anidex
 * AniLibria
 * AnimeClipse
 * Animedia
 * Anime Tosho
 * AniRena
 * AniSource
 * AudioBook Bay (ABB)
 * Badass Torrents
 * BigFANGroup
 * BitRu
 * BT.etree
 * BT4G
 * BTDB
 * BTDIGG
 * BTSOW
 * Byrutor
 * CiliPro (LIAORENCILI)
 * comicat
 * ConCen
 * cpasbien
 * cpasbienClone
 * Demonoid
 * dmhy
 * E-Hentai
 * elitetorrent
 * emtrek
 * Erai-Raws
 * ETTV
 * EXT Torrents
 * ExtraTorrent.cd
 * ExtraTorrent.it
 * EZTV
 * Filebase
 * FireBit
 * Frozen Layer
 * GamesTorrents
 * GkTorrent
 * GloDLS
 * GTorrent
 * GTorrent.pro
 * HDhouse (HDReactor)
 * IBit
 * Idope
 * Il CorSaRo Blu
 * Il Corsaro Nero
 * Internet Archive (archive.org)
 * Isohunt2
 * iTorrent
 * kickasstorrents.ws
 * kickasstorrents.to
 * Legit Torrents
 * LePorno.info
 * LimeTorrents
 * LinuxTracker
 * MacTorrents
 * Magnet4You
 * MejorTorrent
 * MixTapeTorrent
 * Montorrent
 * MoviesDVDR
 * MovieTorrent
 * MyPornClub
 * NewPCT (aka: tvsinpagar, descargas2020, torrentlocura, torrentrapid, tumejortorrent, pctnew, etc)
 * Newstudio
 * Nitro
 * NNTT
 * NoNaMe Club (NNM-Club)
 * Nyaa-Pantsu
 * Nyaa.si
 * OnceSearch
 * OneJAV
 * OxTorrent
 * ParnuXi
 * PC-torrent
 * PiratBit
 * Pirateiro
 * Pornforall
 * PornLeech
 * PornoLive
 * PornoRip
 * PornoTor
 * Portugas
 * ProPorn
 * ProStyleX
 * Rapidzona
 * RARBG
 * RinTor
 * RinTorNeT
 * Rus-media
 * RuTor
 * RuTracker.RU
 * seleZen
 * Sexy-Pics
 * ShizaProject
 * shokweb
 * ShowRSS
 * SkyTorrents.to
 * Solid Torrents
 * sosulki
 * SubsPlease
 * sukebei-Pantsu
 * sukebei.Nyaa.si
 * The Pirate Bay (TPB)
 * TNTfork
 * Tokyo Tosho
 * Torlock
 * TOROS
 * Torrent Downloads (TD)
 * Torrent Oyun indir
 * Torrent Paradise (ML)
 * torrent-pirat
 * Torrent4You
 * Torrent9
 * Torrent9 clone
 * TorrentDownload
 * TorrentFunk
 * TorrentGalaxy (TGx)
 * TorrentKitty
 * TorrentMafya
 * TorrentMax (토렌트맥스)
 * TorrentParadise
 * TorrentProject2
 * TorrentQQ (토렌트큐큐)
 * Torrents.csv
 * TorrentSir (토렌트썰)
 * Torrentv
 * TorrentView (토렌트뷰)
 * TorrentWhiz ( 토렌트위즈)
 * truPornolabs
 * ttobogo
 * Underverse
 * UnionDHT
 * VSTHouse
 * VST Torrents
 * xxxAdultTorrent
 * xxxtor
 * xxxtorrents
 * YourBittorrent
 * YTS.ag
 * zetorrents
 * Zooqle
</details>

<details> <summary> <b> Supported Semi-Private Trackers </b> </summary>

 * AniDUB
 * Anime-Free
 * ArenaBG
 * BaibaKo
 * BookTracker
 * BootyTape
 * CasStudioTV
 * Catorrent
 * Darmowe torrenty
 * Deildu
 * DimeADozen (EzTorrent)
 * DXP (Deaf Experts)
 * EniaHD
 * Erzsebet.pl
 * ExKinoRay
 * Genesis-Movement
 * HamsterStudio
 * HD-CzTorrent
 * HunTorrent
 * IV-Torrents
 * KinoNaVse100
 * Kinorun
 * Kinozal
 * LostFilm.tv
 * Magnetico (Local DHT) [[site](https://github.com/boramalper/magnetico)]
 * MVGroup Forum
 * MVGroup Main
 * Marine Tracker
 * Metal Tracker
 * MuziekFrabriek
 * NetHD (VietTorrent)
 * PornoLab
 * PussyTorrents
 * Rainbow Tracker
 * RiperAM
 * RockBox
 * RuTracker
 * Rustorka
 * SDkino
 * Sharewood
 * SkTorrent
 * SkTorrent-org
 * themixingbowl (TMB)
 * Toloka.to
 * Torrent-Explosiv
 * Torrents-Local
 * TribalMixes
 * Union Fansub
 * YggTorrent (YGG)
 * Ztracker
</details>

<details> <summary> <b> Supported Private Trackers </b> </summary>

 * 0day.kiev
 * 1ptbar
 * 2 Fast 4 You
 * 3ChangTrai (3CT) [![(invite needed)][inviteneeded]](#)
 * 3D Torrents (3DT) [![(invite needed)][inviteneeded]](#)
 * 4thD (4th Dimension)
 * 52PT
 * 720pier
 * Abnormal [![(invite needed)][inviteneeded]](#)
 * ABtorrents (ABT + RNS)
 * Acid Lounge (A-L) [![(invite needed)][inviteneeded]](#)
 * AcrossTheTasman [![(invite needed)][inviteneeded]](#)
 * Aftershock
 * Aidoru!Online
 * Aither
 * AlphaRatio (AR)
 * AmigosShareClub
 * anasch.cc
 * AnimeBytes (AB)
 * AnimeTorrents (AnT)
 * AnimeWorld [![(invite needed)][inviteneeded]](#)
 * Anthelion
 * Araba Fenice (Phoenix) [![(invite needed)][inviteneeded]](#)
 * ArabP2P
 * AsianCinema
 * Asylum Share
 * AudioNews (AN)
 * Aussierul.es [![(invite needed)][inviteneeded]](#)
 * AvistaZ (AsiaTorrents)
 * Borgzelle
 * Back-ups
 * bB
 * BakaBT
 * BeiTai
 * BeyondHD (BHD)
 * Bibliotik
 * BIGTorrent
 * Bit-City Reloaded [![(invite needed)][inviteneeded]](#)
 * BIT-HDTV
 * BiT-TiTAN
 * BitHUmen
 * BitTorrentFiles
 * BiTTuRK
 * Bithorlo (BHO)
 * Bitspyder
 * BJ-Share (BJ)
 * BlueBird [![(invite needed)][inviteneeded]](#)
 * Blutopia (BLU)
 * Boxing Torrents
 * Brasil Tracker
 * BroadCity [![(invite needed)][inviteneeded]](#)
 * BroadcasTheNet (BTN)
 * BrokenStones [![(invite needed)][inviteneeded]](#)
 * BTNext (BTNT)
 * BTSCHOOL
 * BWTorrents
 * CCFBits
 * CGPeers
 * CHDBits
 * Carp-Hunter
 * Carpathians
 * CartoonChaos (CC)
 * CasaTorrent [![(invite needed)][inviteneeded]](#)
 * ChileBT
 * Cinecalidad
 * CinemaMovieS_ZT
 * CinemaZ (EuTorrents)
 * Cinemageddon
 * Cinematik
 * Classix
 * Coastal-Crew
 * Concertos
 * CrazyHD
 * CrazySpirits
 * CrnaBerza
 * DANISH BYTES
 * Darius Tracker
 * Dark-Shadow
 * Dark Tracker
 * Das Unerwartete [![(invite needed)][inviteneeded]](#)
 * DataScene (DS)
 * DesiReleasers
 * DesiTorrents
 * Diablo Torrent
 * DICMusic
 * DigitalCore
 * DivTeam
 * DivxTotal
 * Dragonworld Reloaded [![(invite needed)][inviteneeded]](#)
 * EbookParadijs
 * Ebooks-Shares
 * EfectoDoppler
 * Empornium (EMP)
 * EpubLibre
 * eShareNet
 * eStone (XiDER, BeLoad)
 * ExoticaZ (YourExotic)
 * ExtremeBits
 * ExtremeTorrents [![(invite needed)][inviteneeded]](#)
 * FANO.IN
 * Fantastic Heaven
 * FeedUrNeed
 * Femdomcult
 * FileList (FL)
 * Film-Paleis
 * FinElite (FE)
 * FinVip
 * FocusX
 * Fou-Du-Cinema
 * FreeTorrent
 * FunFile (FF)
 * FunkyTorrents (FT) [![(invite needed)][inviteneeded]](#)
 * Fuzer (FZ)
 * GFXPeers
 * Gay-Torrents.net
 * Gay-Torrents.org [![(invite needed)][inviteneeded]](#)
 * GAYtorrent.ru
 * GazelleGames (GGn) [![(invite needed)][inviteneeded]](#)
 * Generation-Free
 * GigaTorrents
 * GimmePeers (formerly ILT)
 * GiroTorrent
 * GreekDiamond
 * Greek Team
 * HaiDan
 * HD Dolby [![(invite needed)][inviteneeded]](#)
 * HD-Bits.com
 * HD-Forever (HDF)
 * HD-Olimpo
 * HD-Only (HDO)
 * HD-Space (HDS)
 * HD-Spain [![(invite needed)][inviteneeded]](#)
 * HD-Torrents (HDT)
 * HD4FANS [![(invite needed)][inviteneeded]](#)
 * HDArea (HDA)
 * HDAtmos
 * HDBits
 * HDCenter [![(invite needed)][inviteneeded]](#)
 * HDChina (HDWing)
 * HDC (HDCiTY)
 * HDCity
 * HDHome (HDBigger)
 * HDME
 * HDRoute [![(invite needed)][inviteneeded]](#)
 * HDSky
 * HDTime
 * HDTorrents.it
 * HDTurk [![(invite needed)][inviteneeded]](#)
 * HDU [![(invite needed)][inviteneeded]](#)
 * HDZone
 * Hebits
 * HellasTZ
 * Hon3y HD
 * HQSource (HQS)
 * HuSh [![(invite needed)][inviteneeded]](#)
 * IPTorrents (IPT)
 * ImmortalSeed (iS)
 * Immortuos
 * Insane Tracker
 * IPTorrents (IPT)
 * JPopsuki
 * JPTV
 * Karagarga
 * Keep Friends
 * LastFiles
 * LatinoP2P
 * Le Saloon
 * LemonHD
 * LearnFlakes
 * LegacyHD (HD4Free)
 * Libble
 * LibraNet (LN)
 * LinkoManija
 * LosslessClub
 * M-Team TP (MTTP)
 * MaDs Revolution
 * magic-heaven
 * Magico (Trellas)
 * Majomparádé (TurkDepo)
 * MeseVilág (Fairytale World)
 * MicroBit (µBit)
 * Milkie
 * MMA-Torrents
 * MNV (Max-New-Vision)
 * Mononoké-BT [![(invite needed)][inviteneeded]](#)
 * MoreThanTV (MTV)
 * MyAnonamouse (MAM)
 * MySpleen [![(invite needed)][inviteneeded]](#)
 * NBTorrents [![(invite needed)][inviteneeded]](#)
 * NCore
 * Nebulance (NBL) (TransmiTheNet)
 * NetCosmo
 * NetLab
 * NorBits
 * Nordic+
 * Oasis
 * Obscure
 * oMg[WtF]trackr
 * OpenCD
 * Oppaitime [![(invite needed)][inviteneeded]](#)
 * Orpheus
 * OshenPT
 * Ourbits (HDPter)
 * P2PBG
 * P2PElite
 * PassThePopcorn (PTP)
 * Peers.FM
 * Pirata Digital
 * PirateTheNet (PTN)
 * PixelCove (Ultimate Gamer)
 * PiXELHD (PxHD) [![(invite needed)][inviteneeded]](#)
 * Pleasuredome
 * PolishSource (PS)
 * PolishTracker
 * PornBits (PB)
 * Pornbay [![(invite needed)][inviteneeded]](#)
 * PotUK
 * Pretome
 * PrivateHD (PHD)
 * ProAudioTorrents (PAT)
 * PTerClub
 * PTFiles (PTF)
 * PThome
 * PTMSG
 * PTSBAO
 * PTtime
 * PuntoTorrent
 * PuroVicio
 * Puur-Hollands
 * PWTorrents (PWT)
 * R3V WTF! [![(invite needed)][inviteneeded]](#)
 * Racing4Everyone (R4E)
 * RacingForMe (RFM)
 * RedBits
 * Red Star Torrent (RST) [![(invite needed)][inviteneeded]](#)
 * Redacted (PassTheHeadphones)
 * RetroFlix
 * RevolutionTT
 * ROFD
 * Romanian Metal Torrents (RMT) [![(invite needed)][inviteneeded]](#)
 * RPTorrents
 * SceneHD
 * ScenePalace (SP)
 * SceneRush
 * SceneTime
 * SDBits [![(invite needed)][inviteneeded]](#)
 * Secret Cinema
 * SeedFile (SF)
 * ShareFiles
 * Shareisland
 * Shazbat
 * SiamBIT
 * SnowPT (SSPT)
 * SoulVoice [![(invite needed)][inviteneeded]](#)
 * SpeedApp (SceneFZ, XtreMeZone / MYXZ, ICE Torrent)
 * SpeedCD
 * Speedmaster HD
 * SpeedTorrent Reloaded
 * Spirit of Revolution [![(invite needed)][inviteneeded]](#)
 * SportHD [![(invite needed)][inviteneeded]](#)
 * SportsCult
 * SpringSunday
 * SugoiMusic
 * Superbits (SBS)
 * Tapochek
 * Tasmanit [![(invite needed)][inviteneeded]](#)
 * TeamHD
 * TeamOS
 * TEKNO3D [![(invite needed)][inviteneeded]](#)
 * TellyTorrent
 * teracod (Movie Zone)
 * The Falling Angels (TFA)
 * The Geeks [![(invite needed)][inviteneeded]](#)
 * The Horror Charnel (THC)
 * The New Retro
 * The Occult [![(invite needed)][inviteneeded]](#)
 * The Place [![(invite needed)][inviteneeded]](#)
 * The Shinning (TsH)
 * The Show [![(invite needed)][inviteneeded]](#)
 * The Vault [![(invite needed)][inviteneeded]](#)
 * TheAudioScene
 * TheEmpire (TE) [![(invite needed)][inviteneeded]](#)
 * TheLeachZone
 * TheScenePlace (TSP)
 * TJUPT
 * TLFBits [![(invite needed)][inviteneeded]](#)
 * ToTheGlory (TTG)
 * Torrent Network (TN)
 * Torrent Sector Crew (TSC)
 * Torrent Surf
 * Torrent-Syndikat [![(invite needed)][inviteneeded]](#)
 * TOrrent-tuRK (TORK)
 * Torrent.LT
 * TorrentBD
 * TorrentBytes (TBy)
 * TorrentCCF (TCCF)
 * TorrentDay (TD)
 * TorrentDB
 * TorrentFactory
 * TorrentHR
 * TorrentHeaven [![(invite needed)][inviteneeded]](#)
 * TorrentLeech (TL)
 * TorrentLeech.pl
 * TorrentSeeds (TS)
 * Torrentech (TTH)
 * Torrenting (TT) [![(invite needed)][inviteneeded]](#)
 * Torrentland
 * TotallyKids (TK)
 * Trackeros
 * TranceTraffic [![(invite needed)][inviteneeded]](#)
 * Trezzor
 * TTsWEB
 * TurkSeed
 * TurkTorrent (TT)
 * TV Chaos UK (TVCUK)
 * TV-Vault
 * TVstore
 * Twilight Torrents
 * Twilights Zoom
 * U2 (U2分享園@動漫花園) [![(invite needed)][inviteneeded]](#)
 * UHDBits
 * UnionGang [![(invite needed)][inviteneeded]](#)
 * UnlimitZ
 * Vizuk
 * WDT (Wrestling Desires Torrents / Ultimate Wrestling Torrents)
 * Witch-Hunter (Demon-Site)
 * wOOt [![(invite needed)][inviteneeded]](#)
 * World-In-HD [![(invite needed)][inviteneeded]](#)
 * x-ite.me (XM) [![(invite needed)][inviteneeded]](#)
 * xBytesV2
 * XSpeeds (XS)
 * XWT-Classics
 * XWTorrents (XWT)
 * Xthor
 * YDYPT
 * Zamunda.net
 * Zelka.org
 * ZonaQ
</details>

Trackers marked with [![(invite needed)][inviteneeded]](#) have no active maintainer and may be missing features or be broken. If you have an invite for them please send it to garfieldsixtynine -at- gmail.com to get them fixed/improved.


## Support

Kindly report any issues/broken-parts/bugs on [github](https://github.com/dockserver/dockserver/issues) or [discord](https://discord.gg/A7h7bKBCVa)

* Join our [![Discord: https://discord.gg/A7h7bKBCVa](https://img.shields.io/badge/Discord-gray.svg?style=for-the-badge)](https://discord.gg/A7h7bKBCVa) for Support
