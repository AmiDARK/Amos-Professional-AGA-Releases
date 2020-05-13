# About official AMOS Professional Source Code repository.
> On 2020.04.26, François Lionet officially released Amos Professional source code on his own GitHub repository under MIT Licence type as it was initially planed by himself many years ago.<br>
> The link to get access to the official AMOS-Professional-Offical repository Source Code is here : https://github.com/Francaoz/AMOS-Professional-Official<br>
> The original AMOS-Professional-Official licence s available in the License.txt file of this project.<br>
> On 2020.05.01 François Lionet announced officially on his Facebook Page that he gives to Colin Vella the responsability to handle the Amos Professional Official Source Code GitHub repository. ( https://www.facebook.com/photo.php?fbid=10222434008617360&set=a.3542674563888&type=3&theater )

# About AMOS Professional X for AGA support.
> The project that did initially takes the name "Amos Professional X" was stopped. With the official release of Amos Professional under MIT Licence, I have reopened this project.
For the moment Source code is private but it will be released under the original MIT Licence when everything will be finished.

> I have much respect about the huge amount of work François did to create AMOS and AMOS Professional but, for the moment, and in respect to the MIT Licence terms capabilities (source : https://github.com/Francaoz/AMOS-Professional-Official/blob/master/LICENSE seen in the GitHub box about MIT Licence "A short and simple permissive license with conditions only requiring preservation of copyright and license notices. Licensed works, modifications, and larger works may be distributed under different terms and without source code." ) and not restricted by licence information added by François, I consider that improving AMOS Professional with AGA support is a larger work as it require me to makes many changes in many components of the AMOS Professional engine (copper list, sprites, bob, iff/ilbm, load/save datas, internal structures, etc.).<br>
With these, I prefer not release the source code for the moment.<br>
Source code will probably be released for "educational purposes" when the project will be finished (and more especially because it was initially planed with the AMOS Factory team to include this major update inside their major updates, and I want to respect this engagment with the AMOS Factory team)

# 2020.05.06 : Project reorganization

During integration of AGA support to the original Amos Professional 2.00 (ECS), I discovered that due to the fact that AMOS Professional uses static structures for datas such as packed screen, blitter objects, icons, screens, but not only these; I had to made changes that did potentially break double direction compatibility between original Amos Professional 2.00 (ECS) and new Amos Professional 3.00 AGA (X version). Rework entirely the bank system and data structure to be dynamic should be too long, and may not assure a total compatibility between original Amos Professional 2.00 (ECS) and new Amos Professional 3.00 AGA (X version).

This problem forces me to take a decision concerning the future of the development of AGA support for Amos Professional :

 I must proceed to a complete reorganization of both Source Code, and file names for the releases.

This mean, for example, that the new Amos Professional AGA 3.00 will use an AmosProAGA.library instead of the original AMOS.library.
This was required to be sure that any Amiga users can have both original Amos Professional 2.00  (ECS) and Amos Professional 3.00 AGA (X version) capable of running without conflicts on the same computer.
It also ensures that games already developed under the original Amos Professional 2.00  (ECS) can run without problem when Amos Professional 3.0 AGA (X version) is also installed in the computer configuration.
This reorganization also required to update the editor, interpreter and compiler configuration files with a new name including AGA inside, for the same reasons than the ones explained above.
>It is a restart of the whole project concerning AGA support, and as it is a "free time" development (not commercial), I can promise nothing about future releases/updates dates.

I hope that everything will be ok with François Lionet now as I don't want to steal his work. Just protect mine. I hope he can understand this.

François Lionet MIT Licence is available in this project, in the file Licence.txt
The Amos Professional AGA (X version) project ia distribued under MIT License with Closed source.

Regards,
Frédéric Cordier
