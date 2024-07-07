<!--
Created/Authored/coded by : Dileep Verma (DySP (P) - 66th batch) and Soumyashree Behera
Date : 5 January,2024
-->

<!Advocate Dileep Verma>
<html>

<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet">
  <style>
    body {
      font-family: 'Open Sans', sans-serif;
      background-color: #beddf7;
      margin: 0;
      padding: 0;
      text-align: center;
      /* background-image: url('BHARAT.png') ;
            background-size: 25% ;
            background-position: center ;
            back
            background-repeat: no-repeat;
            background-blend-mode: soft-light; */
    }

    #gupta {
      margin-right: 20px;
      position: relative;
      margin-top: 20px;
      margin-left: 1200px;
    }

    #gaurav {
      position: relative;
      top: 20px;
      left: 20px;
      z-index: 999;
      display: inline-block;
    }

    #weight {
      height: 35px;
      width: 200 px;
      text-align: center;
      border: 3px solid;
      font-weight: bolder;
      font-size: 16;
    }

    .button {
      background-color: rgb(8, 182, 13);
      width: 200px;
      font-size: 20px;
      padding: 10px;
      border-radius: 5px;
      border: 3px solid rgb(0, 0, 0);
      color: rgb(255, 255, 255);
      text-align: center;
      margin-right: 20px;
      font-weight: bold;
    }

    .mybtn {
      color: rgb(71, 238, 91);
      font-weight: bold;
      height: auto;
      width: auto;
    }

    #search-box {
      width: 300px;
      padding: 10px;
      font-size: 25;
      border: none;
      border-radius: 5px;
      background-color: #ffffff;
      box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    }

    .autocomplete-items {
      position: absolute;
      top: calc(100% + 3px);
      left: 0;
      right: 0;
      border: 0px solid #d4d4d4;
      border-radius: 5px;
      max-height: fit-content;
      overflow-y: auto;
      background-color: #ffffff;
      box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
      z-index: 998;
      text-align: left;
    }

    .autocomplete-item {
      padding: 10px;
      cursor: pointer;
    }

    .autocomplete-item:hover {
      background-color: #f1f1f1;
    }

    .container {
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
      text-align: centre;
    }

    .btn {
      background-color: WHITE;
      color: RED;
      padding: 9px 18px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
      margin-top: 10px;
      font-weight: bold;
    }

    #panel {
      background-color: #b8e9fc;
      border-radius: 10px;
      box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
      padding: 20px;
      margin-top: 20px;
      align-items: center;
    }

    h1,
    h2,
    h3,
    h4 {
      text-align: center;
      color: #333333;
    }

    h2 {
      font-style: italic;
    }
  </style>
</head>

<body>

  <div id="gaurav">
    <input type="text" id="search-box" placeholder="Type Keyword to Search old IPC Section">
    <div class="autocomplete-items" id="autocomplete-items"></div>

  </div>

  <div class="container">

    <div class="panel">
      <h3>Indian Penal Code to Bhartiya Nyay Sanhita,2023</h3>
      <form class="grv">
        <div id="weightInput">
          <input id="weight" placeholder="Enter IPC Section">
        </div>
        <button type="button" class="btn" id="mybtn" onclick="calculate()">CLICK</button>
      </form>
      <h4>Bhartiya Nyay Sanhita,2023 Section:</h4>
      <div id="results"></div>
    </div>
  </div>
  <h4>Created By : - Dileep Verma</h4>
  <h3>Contact +91 6388714022</h3>
  <h3>Email I'D :- aikawabarhaj@gmail.com</h3>

  <script>
    const data = [
      ` 1 :   Title and extent of operation of the Code.  `,
      ` 2 :   Punishment of offences committed within India.  `,
      ` 3 :   Punishment of offences committed beyond, but which by law may be tried within, India.  `,
      ` 4 :   Extension of Code to extra-territorial offences.  `,
      ` 5 :   Certain laws not to be affected by this Act.  `,
      ` 6 :   Definitions in the Code to be understood subject to exceptions.  `,
      ` 7 :   Sense of expression once explained.  `,
      ` 8 :   Gender.  `,
      ` 9 :   Number.  `,
      ` 10 :   “Man”. “Woman”.  `,
      ` 11 :   “Person”.  `,
      ` 12 :   “Public”.  `,
      ` 13 :   [Omitted.].  `,
      ` 14 :   “Servant of Government”.  `,
      ` 15 :   [Repealed.].  `,
      ` 16 :   [Repealed.].  `,
      ` 17 :   “Government”.  `,
      ` 18 :   “India”.  `,
      ` 19 :   “Judge”.  `,
      ` 20 :   “Court of Justice”.  `,
      ` 21 :   “Public servant”.  `,
      ` 22 :   “Moveable property”.  `,
      ` 23 :   “Wrongful gain”. “Wrongful loss”. Gaining wrongfully/ Losing wrongfully.  `,
      ` 24 :   “Dishonestly”.  `,
      ` 25 :   “Fraudulently”.  `,
      ` 26 :   “Reason to believe”.  `,
      ` 27 :   Property in possession of wife, clerk or servant.  `,
      ` 28 :   “Counterfeit”.  `,
      ` 29 :   “Document”.  `,
      ` 29A. :   “Electronic record”.  `,
      ` 30 :   “Valuable security”.  `,
      ` 31 :   “A will”.  `,
      ` 32 :   Words referring to acts include illegal omissions.  `,
      ` 33 :   “Act”. “Omission”.  `,
      ` 34 :   Acts done by several persons in furtherance of common intention.  `,
      ` 35 :   When such an act is criminal by reason of its being done with a criminal knowledge or intention.  `,
      ` 36 :   Effect caused partly by act and partly by omission.  `,
      ` 37 :   Co-operation by doing one of several acts constituting an offence.  `,
      ` 38 :   Persons concerned in criminal act may be guilty of different offences.  `,
      ` 39 :   “Voluntarily”.  `,
      ` 40 :   “Offence”.  `,
      ` 41 :   “Special law”.  `,
      ` 42 :   “Local law”.  `,
      ` 43 :   “Illegal”. “Legally bound to do”.  `,
      ` 44 :   “Injury”.  `,
      ` 45 :   “Life”.  `,
      ` 46 :   “Death”.  `,
      ` 47 :   “Animal”.  `,
      ` 48 :   “Vessel”.  `,
      ` 49 :   “Year”. “Month”.  `,
      ` 50 :   “Section”.  `,
      ` 51 :   “Oath”.  `,
      ` 52 :   “Good faith”.  `,
      ` 52A. :   “Harbour-“.  `,
      ` 53 :   Punishments.  `,
      ` 53A. :   Construction of reference to transportation.  `,
      ` 54 :   Commutation of sentence of death.  `,
      ` 55 :   Commutation of sentence of imprisonment for life.  `,
      ` 55A. :   Definition of "appropriate Government".  `,
      ` 56 :   [Repealed.].  `,
      ` 57 :   Fractions of terms of punishment.  `,
      ` 58 :   [Repealed.].  `,
      ` 59 :   [Repealed.].  `,
      ` 60 :   Sentence may be (in certain cases of imprisonment) wholly or partly rigorous of simple.  `,
      ` 61 :   [Repealed.].  `,
      ` 62 :   [Repealed.].  `,
      ` 63 :   Amount of fine.  `,
      ` 64 :   Sentence of imprisonment for non-payment of fine.  `,
      ` 65 :   Limit to imprisonment for non-payment of fine, when imprisonment and fine awardable.  `,
      ` 66 :   Description of imprisonment for non-payment of fine.  `,
      ` 67 :   Imprisonment for non-payment of fine, when offence punishable with fine only.  `,
      ` 68 :   Imprisonment to terminate on payment of fine.  `,
      ` 69 :   Termination of imprisonment on payment of proportional part of fine.  `,
      ` 70 :   Fine leviable within six years, or during imprisonment. Death not to discharge property from liability.  `,
      ` 71 :   Limit of punishment of offence made up of several offences.  `,
      ` 72 :   Punishment of person guilty of one of several offences, the judgment stating that it is doubtful of which.  `,
      ` 73 :   Solitary confinement.  `,
      ` 74 :   Limit of solitary confinement.  `,
      ` 75 :   Enhanced punishment for certain offences under Chapter XII or Chapter XVII after previous conviction.  `,
      ` 76 :   Act done by a person bound, or by mistake of fact believing himself bound, by law.  `,
      ` 77 :   Act of Judge when acting judicially.  `,
      ` 78 :   Act done pursuant to the judgment or order of Court.  `,
      ` 79 :   Act done by a person justified, or by mistake of fact believing himself justified, by law.  `,
      ` 80 :   Accident in doing a lawful act.  `,
      ` 81 :   Act likely to cause harm, but done without criminal intent, and to prevent other harm.  `,
      ` 82 :   Act of a child under seven years of age.  `,
      ` 83 :   Act of a child above seven and under twelve of immature understanding.  `,
      ` 84 :   Act of a person of unsound mind.  `,
      ` 85 :   Act of a person incapable of judgment by reason of intoxication caused against his will.  `,
      ` 86 :   Offence requiring a particular intent or knowledge committed by one who is intoxicated.  `,
      ` 87 :   Act not intended and not known to be likely to cause death or grievous hurt, done by consent.  `,
      ` 88 :   Act not intended to cause death, done by consent in good faith for a person's benefit.  `,
      ` 89 :   Act done in good faith for benefit of child or insane person, by or by consent of guardian. Provisos.  `,
      ` 90 :   Consent known to be given under fear or misconception. Consent of insane person. Consent of child.  `,
      ` 91 :   Exclusion of acts which are offences independently of harm caused.  `,
      ` 92 :   Act done in good faith for benefit of a person without consent. Provisos.  `,
      ` 93 :   Communication made in good faith.  `,
      ` 94 :   Act to which a person is compelled by threats.  `,
      ` 95 :   Act causing slight harm. Of the Right of Private Defense  `,
      ` 96 :   Things done in private defence.  `,
      ` 97 :   Right of private defence of the body and of property.  `,
      ` 98 :   Right of private defence against the act of a person of unsound mind, etc.  `,
      ` 99 :   Acts against which there is no right of private defence. Extent to which the right may be exercised.  `,
      ` 100 :   When the right of private defence of the body extends to causing death.  `,
      ` 101 :   When such right extends to causing any harm other than death.  `,
      ` 102 :   Commencement and continuance of the right of private defence of the body.  `,
      ` 103 :   When the right of private defence of property extends to causing death.  `,
      ` 104 :   When such right extends to causing any harm other than death.  `,
      ` 105 :   Commencement and continuance of the right of private defence of property.  `,
      ` 106 :   Right of private defence against deadly assault when there is risk of harm to an innocent person.  `,
      ` 107 :   Abetment of a thing.  `,
      ` 108 :   Abettor.  `,
      ` 108A. :   Abetment in Indian of offences outside India.  `,
      ` 109 :   Punishment of abetment if the act abetted is committed in consequence and when no express provision is made for its punishment.  `,
      ` 110 :   Punishment of abetment if the person abetted does an act with a different intention from that of the abettor.  `,
      ` 111 :   Liability of abettor when one act abetted and different act done.  `,
      ` 112 :   Abettor when liable to cumulative punishment for act abetted and for act done.  `,
      ` 113 :   Liability of abettor for an effect caused by the act abetted different from that intended by the abettor.  `,
      ` 114 :   Abettor present when the offence is committed.  `,
      ` 115 :   Abetment of offence punishable with death or imprisonment for life.  `,
      ` 116 :   Abetment of offence punishable with imprisonment.  `,
      ` 117 :   Abetting commission of offence by the public or by more than ten persons.  `,
      ` 118 :   Concealing design to commit offence punishable with death or imprisonment for life.  `,
      ` 119 :   Public servant concealing design to commit offence.  `,
      ` 120 :   Concealing design to commit offence punishable with imprisonment.  `,
      ` 120A :   Definition of criminal conspiracy.  `,
      ` 120B :   Punishment of criminal conspiracy.  `,
      ` 121 :   Waging, or attempting to wage war, or abetting waging of war, against the Government of India.  `,
      ` 121A :   Conspiracy to commit offences punishable by section 121.  `,
      ` 122 :   Collecting arms, etc., with intention of waging war against the Government of India.  `,
      ` 123 :   Concealing with intent to facilitate design to wage war.  `,
      ` 124 :   Assaulting President, Governor, etc., with intent to compel or restrain the exercise of any lawful power.  `,
      ` 124A :   Sedition.  `,
      ` 125 :   Waging war against any Asiatic power in alliance with the Government of India.  `,
      ` 126 :   Committing depredation on territories of power at peace with the Government of India.  `,
      ` 127 :   Receiving property taken by war or depredation.  `,
      ` 128 :   Public servant voluntarily allowing prisoner of State or war to escape.  `,
      ` 129 :   Public servant negligently suffering such prisoner to escape.  `,
      ` 130 :   Aiding escape of, rescuing or harbouring such prisoner.  `,
      ` 131 :   Abetting mutiny, or attempting to seduce a soldier, sailor, or airman from his duty.  `,
      ` 132 :   Abetment of mutiny.  `,
      ` 133 :   Abetment of assault by soldier, sailor, or airman on his superior officer.  `,
      ` 134 :   Abetment of such assault.  `,
      ` 135 :   Abetment of desertion of soldier, sailor, or airman.  `,
      ` 136 :   Harbouring deserter.  `,
      ` 137 :   Deserter concealed on board merchant vessel through negligence of master.  `,
      ` 138 :   Abetment of act of insubordination by soldier, sailor, or airman.  `,
      ` 138A :   [Repealed].  `,
      ` 139 :   Persons subject to certain Acts.  `,
      ` 140 :   Wearing garb or carrying token used by soldier, sailor, or airman.  `,
      ` 141 :   Unlawful assembly.  `,
      ` 142 :   Being member of unlawful assembly.  `,
      ` 143 :   Punishment for unlawful assembly.  `,
      ` 144 :   Joining unlawful assembly armed with deadly weapon.  `,
      ` 145 :   Joining or continuing in unlawful assembly, knowing it has been commanded to disperse.  `,
      ` 146 :   Rioting.  `,
      ` 147 :   Punishment for rioting.  `,
      ` 148 :   Rioting, armed with deadly weapon.  `,
      ` 149 :   Every member of unlawful assembly guilty of offence committed in prosecution of common object.  `,
      ` 150 :   Hiring, or conniving at hiring, of persons to join unlawful assembly.  `,
      ` 151 :   Knowingly joining or continuing in assembly of five or more persons after it has been commanded to disperse.  `,
      ` 152 :   Assaulting or obstructing public servant when suppressing riot.  `,
      ` 153 :   Wantonly giving provocation, with intent to cause riot.  `,
      ` 153A :   Promoting enmity between different groups on various grounds.  `,
      ` 153AA :   Punishment for knowingly carrying arms in any procession or organizing, or holding or taking part in any mass drill or mass training with arms.  `,
      ` 153B :   Imputation, assertions prejudicial to national-integration.  `,
      ` 154 :   Owner or occupier of land on which an unlawful assembly is held.  `,
      ` 155 :   Liability of person for whose benefit riot is committed.  `,
      ` 156 :   Liability of agent of owner or occupier for whose benefit riot is committed.  `,
      ` 157 :   Harbouring persons hired for an unlawful assembly.  `,
      ` 158 :   Being hired to take part in an unlawful assembly or riot; or to go armed.  `,
      ` 159 :   Affray.  `,
      ` 160 :   Punishment for committing affray.  `,
      ` 166 :   Public servant disobeying law, with intent to cause injury to any person.  `,
      ` 166A :   Public servant disobeying direction under law.  `,
      ` 166B :   Punishment for non-treatment of victim.  `,
      ` 167 :   Public servant framing an incorrect document with intent to cause injury.  `,
      ` 168 :   Public servant unlawfully engaging in trade.  `,
      ` 169 :   Public servant unlawfully buying or bidding for property.  `,
      ` 170 :   Personating a public servant.  `,
      ` 171D :   Personation at elections.  `,
      ` 171E :   Punishment for bribery.  `,
      ` 171F :   Punishment for undue influence or personation at an election.  `,
      ` 171G :   False statement in connection with an election.  `,
      ` 171H :   Illegal payments in connection with an election.  `,
      ` 171-I :   Failure to keep election accounts.  `,
      ` 172 :   Absconding to avoid service of summons or other proceeding.  `,
      ` 173 :   Preventing service of summons or other proceeding, or preventing publication thereof.  `,
      ` 174 :   Non-attendance in obedience to an order from public servant.  `,
      ` 174A :   Non-appearance in response to a proclamation under section 82 of Act 2 of 1974.  `,
      ` 175 :   Omission to produce document to public servant by person legally bound to produce it.  `,
      ` 176 :   Omission to give notice or information to public servant by person legally bound to give it.  `,
      ` 177 :   Furnishing false information.  `,
      ` 178 :   Refusing oath or affirmation when duly required by public servant to make it.  `,
      ` 179 :   Refusing to answer public servant authorised to question.  `,
      ` 180 :   Refusing to sign statement.  `,
      ` 181 :   False statement on oath or affirmation to public servant or person authorised to administer an oath or affirmation.  `,
      ` 182 :   False information, with intent to cause public servant to use his lawful power to the injury of another person.  `,
      ` 183 :   Resistance to the taking of property by the lawful authority of a public servant.  `,
      ` 184 :   Obstructing sale of property offered for sale by authority of public servant.  `,
      ` 185 :   Illegal purchase or bid for property offered for sale by authority of public servant.  `,
      ` 186 :   Obstructing public servant in discharge of public functions.  `,
      ` 187 :   Omission to assist public servant when bound by law to give assistance.  `,
      ` 188 :   Disobedience to order duly promulgated by public servant.  `,
      ` 189 :   Threat of injury to public servant.  `,
      ` 190 :   Threat of injury to induce person to refrain from applying for protection to public servant.  `,
      ` 191 :   Giving false evidence.  `,
      ` 192 :   Fabricating false evidence.  `,
      ` 193 :   Punishment for false evidence.  `,
      ` 194 :   Giving or fabricating false evidence with intent to procure conviction of capital offence.  `,
      ` 195 :   Giving or fabricating false evidence with intent to procure conviction of offence punishable with imprisonment.  `,
      ` 195A :   Threatening any person to give false evidence.  `,
      ` 196 :   Using evidence known to be false.  `,
      ` 197 :   Issuing or signing false certificate.  `,
      ` 198 :   Using as true a certificate known to be false.  `,
      ` 199 :   False statement made in declaration which is by law receivable as evidence.  `,
      ` 200 :   Using as true such declaration knowing it to be false.  `,
      ` 201 :   Causing disappearance of evidence of offence, or giving false information, to screen offender.  `,
      ` 202 :   Intentional omission to give information of offence by person bound to inform.  `,
      ` 203 :   Giving false information respecting an offence committed.  `,
      ` 204 :   Destruction of document to prevent its production as evidence.  `,
      ` 205 :   False personation for purpose of act or proceeding in suit or prosecution.  `,
      ` 206 :   Fraudulent removal or concealment of property to prevent its seizure as forfeited or in execution.  `,
      ` 207 :   Fraudulent claim to property to prevent its seizure as forfeited or in execution.  `,
      ` 208 :   Fraudulently suffering decree for sum not due.  `,
      ` 209 :   Dishonestly making false claim in Court.  `,
      ` 210 :   Fraudulently obtaining decree for sum not due.  `,
      ` 211 :   False charge of offence made with intent to injure.  `,
      ` 212 :   Harbouring offender.  `,
      ` 213 :   Taking gift, etc., to screen an offender from punishment.  `,
      ` 214 :   Offering gift or restoration of property in consideration of screening offender.  `,
      ` 215 :   Taking gift to help to recover stolen property, etc.  `,
      ` 216 :   Harbouring offender who has escaped from custody of whose apprehension has been ordered.  `,
      ` 216A :   Penalty for harbouring robbers or dacoits.  `,
      ` 216B :   [Repealed.]  `,
      ` 217 :   Public servant disobeying direction of law with intent to save person from punishment or property from forfeiture.  `,
      ` 218 :   Public servant framing incorrect record or writing with intent to save person from punishment or property from forfeiture.  `,
      ` 219 :   Public servant in judicial proceeding corruptly making report, etc., contrary to law.  `,
      ` 220 :   Commitment for trial or confinement by person having authority who knows that he is acting contrary to law.  `,
      ` 221 :   Intentional omission to apprehend on the part of public servant bound to apprehend.  `,
      ` 222 :   Intentional omission to apprehend on the part of public servant bound to apprehend person under sentence or lawfully committed.  `,
      ` 223 :   Escape from confinement or custody negligently suffered by public servant.  `,
      ` 224 :   Resistance or obstruction by a person to his lawful apprehension.  `,
      ` 225 :   Resistance or obstruction to lawful apprehension of another person.  `,
      ` 225A :   Omission to apprehend, or sufferance of escape, on part of public servant, in cases not otherwise provided for.  `,
      ` 225B :   Resistance or obstruction to lawful apprehension, or escape or rescue in cases not otherwise provided for.  `,
      ` 226 :   [Repealed.]  `,
      ` 227 :   Violation of condition of remission of punishment.  `,
      ` 228 :   Intentional insult or interruption to public servant sitting in judicial proceeding.  `,
      ` 228A :   Disclosure of identity of the victim of certain offences, etc.  `,
      ` 229 :   Personation of a juror or assessor.  `,
      ` 229A :   Failure by person released on bail or bond to appear in Court.  `,
      ` 230 :   Definition of "Coin" and "Indian coin".  `,
      ` 231 :   Counterfeiting coin.  `,
      ` 232 :   Counterfeiting Indian coin.  `,
      ` 233 :   Making or selling instrument for counterfeiting coin.  `,
      ` 234 :   Making or selling instrument for counterfeiting Indian coin.  `,
      ` 235 :   Possession of instrument or material for the purpose of using the same for counterfeiting coin: if Indian coin.  `,
      ` 236 :   Abetting in India the counterfeiting out of India of coin.  `,
      ` 237 :   Import or export of counterfeit coin.  `,
      ` 238 :   Import or export of counterfeits of the Indian coin.  `,
      ` 239 :   Delivery of coin, possessed with knowledge that it is counterfeit.  `,
      ` 240 :   Delivery of Indian coin, possessed with knowledge that it is counterfeit.  `,
      ` 241 :   Delivery of coin as genuine, which, when first possessed, the deliverer did not know to be counterfeit.  `,
      ` 242 :   Possession of counterfeit coin by person who knew it to be counterfeit when he became possessed thereof.  `,
      ` 243 :   Possession of Indian coin by person who knew it to be counterfeit when he became possessed thereof.  `,
      ` 244 :   Person employed in mint causing coin to be of different weight or composition from that fixed by law.  `,
      ` 245 :   Unlawfully taking coining instrument from mint.  `,
      ` 246 :   Fraudulently or dishonestly diminishing weight or altering composition of coin.  `,
      ` 247 :   Fraudulently or dishonestly diminishing weight or altering composition of Indian coin.  `,
      ` 248 :   Altering appearance of coin with intent that it shall pass as coin of different description.  `,
      ` 249 :   Altering appearance of Indian coin with intent that it shall pass as coin of different description.  `,
      ` 250 :   Delivery of coin, possessed with knowledge that it is altered.  `,
      ` 251 :   Delivery of Indian coin, possessed with knowledge that it is altered.  `,
      ` 252 :   Possession of coin by person who knew it to be altered when he became possessed thereof.  `,
      ` 253 :   Possession of Indian coin by person who knew it to be altered when he became possessed thereof.  `,
      ` 254 :   Delivery of coin as genuine which, when first possessed, the deliverer did not know to be altered.  `,
      ` 255 :   Counterfeiting Government stamp.  `,
      ` 256 :   Having possession of instrument or material for counterfeiting Government stamp.  `,
      ` 257 :   Making or selling instrument for counterfeiting Government stamp.  `,
      ` 258 :   Sale of counterfeit Government stamp.  `,
      ` 259 :   Having possession of counterfeit Government stamp.  `,
      ` 260 :   Using as genuine a Government stamp known to be counterfeit.  `,
      ` 261 :   Effacing writing from substance bearing Government stamp, or removing from document a stamp used for it, with intent to cause loss to Government.  `,
      ` 262 :   Using Government stamp known to have been before used.  `,
      ` 263 :   Erasure of mark denoting that stamp has been used.  `,
      ` 263A :   Prohibition of fictitious stamps.  `,
      ` 264 :   Fraudulent use of false instrument for weighing.  `,
      ` 265 :   Fraudulent use of false weight or measure.  `,
      ` 266 :   Being in possession of false weight or measure.  `,
      ` 267 :   Making or selling false weight or measure.  `,
      ` 268 :   Public nuisance.  `,
      ` 269 :   Negligent act likely to spread infection of disease dangerous to life.  `,
      ` 270 :   Malignant act likely to spread infection of disease dangerous to life.  `,
      ` 271 :   Disobedience to quarantine rule.  `,
      ` 272 :   Adulteration of food or drink intended for sale.  `,
      ` 273 :   Sale of noxious food or drink.  `,
      ` 274 :   Adulteration of drugs.  `,
      ` 275 :   Sale of adulterated drugs.  `,
      ` 276 :   Sale of drug as a different drug or preparation.  `,
      ` 277 :   Fouling water of public spring or reservoir.  `,
      ` 278 :   Making atmosphere noxious to health.  `,
      ` 279 :   Rash driving or riding on a public way.  `,
      ` 280 :   Rash navigation of vessel.  `,
      ` 281 :   Exhibition of false light, mark or buoy.  `,
      ` 282 :   Conveying person by water for hire in unsafe or overloaded vessel.  `,
      ` 283 :   Danger or obstruction in public way or line of navigation.  `,
      ` 284 :   Negligent conduct with respect to poisonous substance.  `,
      ` 285 :   Negligent conduct with respect to fire or combustible matter.  `,
      ` 286 :   Negligent conduct with respect to explosive substance.  `,
      ` 287 :   Negligent conduct with respect to machinery.  `,
      ` 288 :   Negligent conduct with respect to pulling down or repairing buildings.  `,
      ` 289 :   Negligent conduct with respect to animal.  `,
      ` 290 :   Punishment for public nuisance in cases not otherwise provided for.  `,
      ` 291 :   Continuance of nuisance after injunction to discontinue.  `,
      ` 292 :   Sale, etc., of obscene books, etc.  `,
      ` 293 :   Sale, etc., of obscene objects to young person.  `,
      ` 294 :   Obscene acts and songs.  `,
      ` 294A :   Keeping lottery office.  `,
      ` 295 :   Injuring or defiling place of worship, with intent to insult the religion of any class.  `,
      ` 295A :   Deliberate and malicious acts, intended to outrage religious feelings of any class by insulting its religion or religious beliefs.  `,
      ` 296 :   Disturbing religious assembly.  `,
      ` 297 :   Trespassing on burial places, etc.  `,
      ` 298 :   Uttering words, etc., with deliberate intent to wound the religious feelings.  `,
      ` 299 :   Culpable homicide.  `,
      ` 300 :   Murder. When culpable homicide is not murder.  `,
      ` 301 :   Culpable homicide by causing death of person other than person whose death was intended.  `,
      ` 302 :   Punishment for murder.  `,
      ` 303 :   Punishment for murder by life-convict.  `,
      ` 304 :   Punishment for culpable homicide not amounting to murder.  `,
      ` 304A :   Causing death by negligence.  `,
      ` 304B :   Dowry death.  `,
      ` 305 :   Abetment of suicide of child or insane person.  `,
      ` 306 :   Abetment of suicide.  `,
      ` 307 :   Attempt to murder. Attempts by life-convicts.  `,
      ` 308 :   Attempt to commit culpable homicide.  `,
      ` 309 :   Attempt to commit suicide.  `,
      ` 310 :   Thug.  `,
      ` 311 :   Punishment.  `,
      ` 312 :   Causing miscarriage.  `,
      ` 313 :   Causing miscarriage without woman's consent.  `,
      ` 314 :   Death caused by act done with intent to cause miscarriage if act done without woman's consent.  `,
      ` 315 :   Act done with intent to prevent child being born alive or to cause it to die after birth.  `,
      ` 316 :   Causing death of quick unborn child by act amounting to culpable homicide.  `,
      ` 317 :   Exposure and abandonment of child under twelve years, by parent or person having care of it.  `,
      ` 318 :   Concealment of birth by secret disposal of dead body.  `,
      ` 319 :   Hurt.  `,
      ` 320 :   Grievous hurt.  `,
      ` 321 :   Voluntarily causing hurt.  `,
      ` 322 :   Voluntarily causing grievous hurt.  `,
      ` 323 :   Punishment for voluntarily causing hurt.  `,
      ` 324 :   Voluntarily causing hurt by dangerous weapons or means.  `,
      ` 325 :   Punishment for voluntarily causing grievous hurt.  `,
      ` 326 :   Voluntarily causing grievous hurt by dangerous weapons or means.  `,
      ` 326A :   Voluntarily causing grievous hurt by use of acid, etc.  `,
      ` 326B :   Voluntarily throwing or attempting to throw acid.  `,
      ` 327 :   Voluntarily causing hurt to extort property, or to constrain to an illegal act.  `,
      ` 328 :   Causing hurt by means of poison, etc., with intent to commit an offence.  `,
      ` 329 :   Voluntarily causing grievous hurt to extort property, or to constrain to an illegal act.  `,
      ` 330 :   Voluntarily causing hurt to extort confession, or to compel restoration of property.  `,
      ` 331 :   Voluntarily causing grievous hurt to extort confession, or to compel restoration of property.  `,
      ` 332 :   Voluntarily causing hurt to deter public servant from his duty.  `,
      ` 333 :   Voluntarily causing grievous hurt to deter public servant from his duty.  `,
      ` 334 :   Voluntarily causing hurt on provocation.  `,
      ` 335 :   Voluntarily causing grievous hurt on provocation.  `,
      ` 336 :   Act endangering life or personal safety of others.  `,
      ` 337 :   Causing hurt by act endangering life or personal safety of others.  `,
      ` 338 :   Causing grievous hurt by act endangering life or personal safety of others.  `,
      ` 339 :   Wrongful restraint.  `,
      ` 340 :   Wrongful confinement.  `,
      ` 341 :   Punishment for wrongful restraint.  `,
      ` 342 :   Punishment for wrongful confinement.  `,
      ` 343 :   Wrongful confinement for three or more days.  `,
      ` 344 :   Wrongful confinement for ten or more days.  `,
      ` 345 :   Wrongful confinement of person for whose liberation writ has been issued.  `,
      ` 346 :   Wrongful confinement in secret.  `,
      ` 347 :   Wrongful confinement to extort property, or constrain to illegal act.  `,
      ` 348 :   Wrongful confinement to extort confession, or compel restoration of property.  `,
      ` 349 :   Force.  `,
      ` 350 :   Criminal force.  `,
      ` 351 :   Assault.  `,
      ` 352 :   Punishment for assault or criminal force otherwise than on grave provocation.  `,
      ` 353 :   Assault or criminal force to deter public servant from discharge of his duty.  `,
      ` 354 :   Assault of criminal force to woman with intent to outrage her modesty.  `,
      ` 354A :   Sexual harassment and punishment for sexual harassment.  `,
      ` 354B :   Assault or use of criminal force to woman with intent to disrobe.  `,
      ` 354C :   Voyeurism.  `,
      ` 354D :   Stalking.  `,
      ` 355 :   Assault or criminal force with intent to dishonour person, otherwise than on grave provocation.  `,
      ` 356 :   Assault or criminal force in attempt to commit theft of property carried by a person.  `,
      ` 357 :   Assault or criminal force in attempt wrongfully to confine a person.  `,
      ` 358 :   Assault or criminal force on grave provocation.  `,
      ` 359 :   Kidnapping.  `,
      ` 360 :   Kidnapping from India.  `,
      ` 361 :   Kidnapping from lawful guardianship.  `,
      ` 362 :   Abduction.  `,
      ` 363 :   Punishment for kidnapping.  `,
      ` 363A :   Kidnapping or maiming a minor for purposes of begging.  `,
      ` 364 :   Kidnapping or abducting in order to murder.  `,
      ` 364A :   Kidnapping for ransom, etc.  `,
      ` 365 :   Kidnapping or abducting with intent secretly and wrongfully to confine person.  `,
      ` 366 :   Kidnapping, abducting or inducing woman to compel her marriage, etc.  `,
      ` 366A :   Procuration of minor girl.  `,
      ` 366B :   Importation of girl from foreign country.  `,
      ` 367 :   Kidnapping or abducting in order to subject person to grievous hurt, slavery, etc.  `,
      ` 368 :   Wrongfully concealing or keeping in confinement, kidnapped or abducted person.  `,
      ` 369 :   Kidnapping or abducting child under ten years with intent to steal from its person.  `,
      ` 370 :   Trafficking of person.  `,
      ` 370A :   Exploitation of a trafficked person.  `,
      ` 371 :   Habitual dealing in slaves.  `,
      ` 372 :   Selling minor for purposes of prostitution, etc.  `,
      ` 373 :   Buying minor for purposes of prostitution, etc.  `,
      ` 374 :   Unlawful compulsory labour.  `,
      ` 375 :   Rape.  `,
      ` 376 :   Punishment for rape.  `,
      ` 376A :   Punishment for causing death or resulting in persistent vegetative state of victim.  `,
      ` 376B :   Sexual intercourse by husband upon his wife during separation.  `,
      ` 376C :   Sexual intercourse by a person in authority.  `,
      ` 376D :   Gang rape.  `,
      ` 376DA :   Punishment for gang rape on woman under sixteen years of age.  `,
      ` 376DB :   Punishment for gang rape on woman under twelve years of age.  `,
      ` 376E :   Punishment for repeat offenders.  `,
      ` 377 :   Unnatural offences.  `,
      ` 378 :   Theft.  `,
      ` 379 :   Punishment for theft.  `,
      ` 380 :   Theft in dwelling house, etc.  `,
      ` 381 :   Theft by clerk or servant of property in possession of master.  `,
      ` 382 :   Theft after preparation made for causing death, hurt or restraint in order to the committing of the theft.  `,
      ` 383 :   Extortion.  `,
      ` 384 :   Punishment for extortion.  `,
      ` 385 :   Putting person in fear of injury in order to commit extortion.  `,
      ` 386 :   Extortion by putting a person in fear of death on grievous hurt.  `,
      ` 387 :   Putting person in fear of death or of grievous hurt, in order to commit extortion.  `,
      ` 388 :   Extortion by threat of accusation of an offence punishable with death or imprisonment for life, etc.  `,
      ` 389 :   Putting person in fear of accusation of offence, in order to commit extortion.  `,
      ` 390 :   Robbery. When theft is robbery. When extortion is robbery.  `,
      ` 391 :   Dacoity.  `,
      ` 392 :   Punishment for robbery.  `,
      ` 393 :   Attempt to commit robbery.  `,
      ` 394 :   Voluntarily causing hurt in committing robbery.  `,
      ` 395 :   Punishment for dacoity.  `,
      ` 396 :   Dacoity with murder.  `,
      ` 397 :   Robbery, or dacoity, with attempt to cause death or grievous hurt.  `,
      ` 398 :   Attempt to commit robbery or dacoity when armed with deadly weapon.  `,
      ` 399 :   Making preparation to commit dacoity.  `,
      ` 400 :   Punishment for belonging to gang of dacoits.  `,
      ` 401 :   Punishment for belonging to gang of thieves.  `,
      ` 402 :   Assembling for purpose of committing dacoity.  `,
      ` 403 :   Dishonest misappropriation of property.  `,
      ` 404 :   Dishonest misappropriation of property possessed by deceased person at the time of his death.  `,
      ` 405 :   Criminal breach of trust.  `,
      ` 406 :   Punishment for criminal breach of trust.  `,
      ` 407 :   Criminal breach of trust by carrier, etc.  `,
      ` 408 :   Criminal breach of trust by clerk or servant.  `,
      ` 409 :   Criminal breach of trust by public, servant. or by banker, merchant or agent.  `,
      ` 410 :   Stolen property.  `,
      ` 411 :   Dishonestly receiving stolen property.  `,
      ` 412 :   Dishonestly receiving property stolen in the commission of a dacoity.  `,
      ` 413 :   Habitually dealing in stolen property.  `,
      ` 414 :   Assisting in concealment of stolen property.  `,
      ` 415 :   Cheating.  `,
      ` 416 :   Cheating by personation.  `,
      ` 417 :   Punishment for cheating.  `,
      ` 418 :   Cheating with knowledge that wrongful loss may ensue to person whose interest offender is bound to protect.  `,
      ` 419 :   Punishment for cheating by personation.  `,
      ` 420 :   Cheating and dishonestly inducing delivery of property.  `,
      ` 421 :   Dishonest or fraudulent removal or concealment of property to prevent distribution among creditor.  `,
      ` 422 :   Dishonestly or fraudulently preventing debt being available for creditors.  `,
      ` 423 :   Dishonest or fraudulent execution of deed of transfer containing false statement of consideration.  `,
      ` 424 :   Dishonest or fraudulent removal or concealment of property.  `,
      ` 425 :   Mischief.  `,
      ` 426 :   Punishment for mischief.  `,
      ` 427 :   Mischief causing damage to the amount of fifty rupees.  `,
      ` 428 :   Mischief by killing or maiming animal of the value of ten rupees.  `,
      ` 429 :   Mischief by killing or maiming cattle, etc., of any value or any animal of the value of fifty rupees.  `,
      ` 430 :   Mischief by injury to works of irrigation or by wrongfully diverting water.  `,
      ` 431 :   Mischief by injury to public road, bridge, river or channel.  `,
      ` 432 :   Mischief by causing inundation or obstruction to public drainage attended with damage.  `,
      ` 433 :   Mischief by destroying, moving or rendering less useful a light-house or sea-mark.  `,
      ` 434 :   Mischief by destroying or moving, etc., a land-mark fixed by public authority.  `,
      ` 435 :   Mischief by fire or explosive substance with intent to cause damage to amount of one hundred or (in case of agricultural produce ) ten rupees.  `,
      ` 436 :   Mischief by fire or explosive substance with intent to destroy house, etc.  `,
      ` 437 :   Mischief with intent to destroy or make unsafe a decked vessel or one of twenty tons burden.  `,
      ` 438 :   Punishment for the mischief described in section 437 committed by fire or explosive substance.  `,
      ` 439 :   Punishment for intentionally running vessel aground, or ashore with intent to commit theft, etc.  `,
      ` 440 :   Mischief committed after preparation made for causing death or hurt.  `,
      ` 441 :   Criminal trespass.  `,
      ` 442 :   House-trespass.  `,
      ` 443 :   Lurking house-trespass.  `,
      ` 444 :   Lurking house-trespass by night.  `,
      ` 445 :   House-breaking.  `,
      ` 446 :   House-breaking by night.  `,
      ` 447 :   Punishment for criminal trespass.  `,
      ` 448 :   Punishment for house-trespass.  `,
      ` 449 :   House-trespass in order to commit offence punishable with death.  `,
      ` 450 :   House-trespass in order to commit offence punishable with imprisonment for life.  `,
      ` 451 :   House-trespass in order to commit offence punishable with imprisonment.  `,
      ` 452 :   House-trespass after preparation for hurt, assault or wrongful restraint.  `,
      ` 453 :   Punishment for lurking house-trespass or house-breaking.  `,
      ` 454 :   Lurking house-trespass or house-breaking in order to commit offence punishable with imprisonment.  `,
      ` 455 :   Lurking house-trespass or house-breaking after preparation for hurt, assault or wrongful restraint.  `,
      ` 456 :   Punishment for lurking house-trespass or house-breaking by night.  `,
      ` 457 :   Lurking house-trespass or house-breaking by night in order to commit offence punishable with imprisonment.  `,
      ` 458 :   Lurking house-trespass or house-breaking by night after preparation for hurt, assault, or wrongful restraint.  `,
      ` 459 :   Grievous hurt caused whilst committing lurking house-trespass or house-breaking.  `,
      ` 460 :   All persons jointly concerned in lurking house-trespass or house-breaking by night punishable.  `,
      ` 461 :   Dishonestly breaking open receptacle containing property.  `,
      ` 462 :   Punishment for same offence when committed by person entrusted with custody.  `,
      ` 463 :   Forgery.  `,
      ` 464 :   Making a false document.  `,
      ` 465 :   Punishment for forgery.  `,
      ` 466 :   Forgery of record of Court or of public register, etc.  `,
      ` 467 :   Forgery of valuable security, will, etc.  `,
      ` 468 :   Forgery for purpose of cheating.  `,
      ` 469 :   Forgery for purpose of harming reputation.  `,
      ` 470 :   Forged document.  `,
      ` 471 :   Using as genuine a forged document or electronic record.  `,
      ` 472 :   Making or possessing counterfeit seal, etc., with intent to commit forgery punishable under section 467.  `,
      ` 473 :   Making or possessing counterfeit seal, etc., with intent to commit forgery punishable otherwise.  `,
      ` 474 :   Having possession of document described in section 466 or 467, knowing it to be forged.  `,
      ` 475 :   Counterfeiting device or mark used for authenticating documents described in section 467.  `,
      ` 476 :   Counterfeiting device or mark used for authenticating documents other than those described in section 467.  `,
      ` 477 :   Fraudulent cancellation, destruction, etc., of will, authority to adopt, or valuable security.  `,
      ` 477A :   Falsification of accounts.  `,
      ` 478 :   [Repealed].  `,
      ` 479 :   Property mark.  `,
      ` 480 :   [Repealed].  `,
      ` 481 :   Using a false property mark.  `,
      ` 482 :   Punishment for using a false property mark.  `,
      ` 483 :   Counterfeiting a property mark used by another.  `,
      ` 484 :   Counterfeiting a mark used by a public servant.  `,
      ` 485 :   Making or possession of any instrument for counterfeiting a property mark.  `,
      ` 486 :   Selling goods marked with a counterfeit property mark.  `,
      ` 487 :   Making a false mark upon any receptacle containing goods.  `,
      ` 488 :   Punishment for making use of any such false mark.  `,
      ` 489 :   Tampering with property mark with intent to cause injury.  `,
      ` 489A :   Counterfeiting currency-notes or bank-notes.  `,
      ` 489B :   Using as genuine, forged or counterfeit currency-notes or bank-notes.  `,
      ` 489C :   Possession of forged or counterfeit currency notes or bank-notes.  `,
      ` 489D :   Making or possessing instruments or materials for forging or counterfeiting currency-notes or bank-notes.  `,
      ` 489E :   Making or using documents resembling currency-notes or bank-notes.  `,
      ` 490 :   [Repealed].  `,
      ` 491 :   Breach of contract to attend on and supply wants of helpless person.  `,
      ` 493 :   Cohabitation caused by a man deceitfully inducing a belief of lawful marriage.  `,
      ` 494 :   Marrying again during life-time of husband or wife.  `,
      ` 495 :   Same offence with concealment of former marriage from person with whom subsequent marriage is contracted.  `,
      ` 496 :   Marriage ceremony fraudulently gone through without lawful marriage.  `,
      ` 497 :   Adultery.  `,
      ` 498 :   Enticing or taking away or detaining with criminal intent a married woman.  `,
      ` 498A :   Husband or relative of husband of a woman subjecting her to cruelty.  `,
      ` 499 :   Defamation.  `,
      ` 500 :   Punishment for defamation.  `,
      ` 501 :   Printing or engraving matter known to be defamatory.  `,
      ` 502 :   Sale of printed or engraved substance containing defamatory matter.  `,
      ` 503 :   Criminal intimidation.  `,
      ` 504 :   Intentional insult with intent to provoke breach of the peace.  `,
      ` 505 :   Statements conducing to public mischief.  `,
      ` 506 :   Punishment for criminal intimidation.  `,
      ` 507 :   Criminal intimidation by an anonymous communication.  `,
      ` 508 :   Act caused by inducing person to believe that he will be rendered an object of the Divine displeasure.  `,
      ` 509 :   Word, gesture or act intended to insult the modesty of a woman.  `,
      ` 510 :   Misconduct in public by a drunken person.  `,
      ` 511 :   Punishment for attempting to commit offences punishable with imprisonment for life or other imprisonment.  `,
    ];
    const searchBox = document.getElementById('search-box');
    const autocompleteItems = document.getElementById('autocomplete-items');
    searchBox.addEventListener('input', function() {
      const inputValue = this.value.toLowerCase();
      autocompleteItems.innerHTML = '';
      if (inputValue.length === 0) {
        return;
      }
      const matchingItems = data.filter(item => item.toLowerCase().includes(inputValue));
      matchingItems.forEach(item => {
        const index = item.toLowerCase().indexOf(inputValue);
        const highlighted = item.substring(0, index) + "<strong>" + item.substring(index, index + inputValue.length) + "</strong>" + item.substring(index + inputValue.length);
        const autocompleteItem = document.createElement('div');
        autocompleteItem.innerHTML = highlighted;
        autocompleteItem.classList.add('autocomplete-item');
        autocompleteItem.addEventListener('click', function() {
          searchBox.value = item;
          autocompleteItems.innerHTML = '';
        });
        autocompleteItems.appendChild(autocompleteItem);
      });
    });
    document.addEventListener('click', function(e) {
      if (!autocompleteItems.contains(e.target)) {
        autocompleteItems.innerHTML = '';
      }
    });
  </script>

  <script src="ipcAdInfo.js"></script>
</body>

</html>
