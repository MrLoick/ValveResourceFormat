# Valve Resource Format

[![Build Status (Travis)](https://img.shields.io/travis/SteamDatabase/ValveResourceFormat/master.svg?label=Travis&style=flat-square)](https://travis-ci.org/SteamDatabase/ValveResourceFormat)
[![Build Status (AppVeyor)](https://img.shields.io/appveyor/ci/xPaw/valveresourceformat/master.svg?label=AppVeyor&style=flat-square)](https://ci.appveyor.com/project/xPaw/valveresourceformat)
[![Coverage Status](https://img.shields.io/coveralls/SteamDatabase/ValveResourceFormat.svg?label=Test Coverage&style=flat-square)](https://coveralls.io/github/SteamDatabase/ValveResourceFormat)
[![NuGet](https://img.shields.io/nuget/v/ValveResourceFormat.svg?label=NuGet&style=flat-square)](https://www.nuget.org/packages/ValveResourceFormat/)

Valve's Source 2 resource file format *(also known as Stupid Valve Format)* parser and decompiler. Contents of this repository are available under [MIT](LICENSE) license.

**Interested in helping? Jump in `#steamdb` on [freenode](https://freenode.net/) and ask away!**

This repository is split into three components:
- *CLI Decompiler* - File viewer, decompiler and a playground for testing new formats and features.
- *GUI Viewer* - A complete mess of winforms and other fun things.
- *Library* - The only sane part of this repository, provides public API.

## What's supported?
- Sound player
- Model viewer
- VPK viewer which supports opening and exporting files
- Read only VPK API
- Binary KeyValues3 parser
- NTRO support

### Supported resource types
Ext      | Name                    | Support
-------- | ----------------------- | -------
vanim    | Animation               | No
vagrp    | Animation Group         | No
vseq     | Sequence Group          | No
vpcf     | Particle System         | :+1: NTRO, KV3
vmat     | Material                | :+1: NTRO
vmks     | Sheet                   | No
vmesh    | Mesh                    | Vertex and index buffers, vertex attributes
vtex     | Compiled Texture        | :+1: RGBA8888, RGBA16161616F, DXT1, DXT5, PNG
vmdl     | Model                   | Started
vphys    | Physics Collision Mesh  | No
vsnd     | Sound                   | :+1: wav, mp3
vmorf    | MorphSet                | No
vrman    | ResourceManifest        | No
vwrld    | World                   | No
vwnod    | WorldNode               | No
vvis     | WorldVisibility         | No
vents    | EntityLump              | No
vsurf    | Surface Properties      | No
vsndevts | Sound Event Script      | No
vsndstck | Sound Stack Script      | No
vfont    | Bitmap Font             | No
vrmap    | Resource Remap Table    | No
vcss     | Panorama Style          | :+1:
vxml     | Panorama Layout         | :+1:
vpdi     | Panorama Dynamic Images | No
vjs      | Panorama Script         | :+1:
vpsf     | Particle Snapshot       | No
vmap     | Map                     | No

Not all formats are 100% supported, some parameters are still unknown and not fully understood.

## Eye catchy screenshots
<table>
	<tr>
		<td><img src="https://steamdatabase.github.io/ValveResourceFormat/static/screen_glados.png"></td>
		<td><img src="https://steamdatabase.github.io/ValveResourceFormat/static/screen_potato.png"></td>
	</tr>
	<tr>
		<td><img src="https://steamdatabase.github.io/ValveResourceFormat/static/screen_vpk.png"></td>
		<td><img src="https://steamdatabase.github.io/ValveResourceFormat/static/screen_cli.png"></td>
	</tr>
</table>
