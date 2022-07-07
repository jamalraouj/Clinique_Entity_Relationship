# Clinique_Entity_Relationship
https://app.gleek.io/diagrams/NWTOWK03hLC3C7SWVbd-xw
Medecin
	int id_medecin
	var nom_medecin
	var telephone
	var adresse
	var CIN
	text experience
	int salaire
	var temps_travail
	var jour_travail
	var status_medecin
	date joindre_a
	date mise_a_jour_a



Specialite
	int id_specialite 
	var nom
	text description

Maladie
	int id_maladie
	var nom_maladie
	text description


dossier
	int id_dossier
	var CIN
	var title
	var nom_patient
	date date_maintenant
	text cahier_santé
	var pass-vaccinal
	int fk_medecin
	int fk_chambre
	int fk_medicament
	var profession
	var status_dossier
	int fk_rendezvous
Admission
	int id_admission
	int fk_patient
	TimeStamp date
patient
	int id_patient
	int nom_patient
	var CIN
	var fk_dossier
	var status_patient
Rendez_vous
	int id_rendez_vous
	var CIN
	DateTime date_rendezvous
	TimeStamp date
//pyment type	
Encaissements
	int id_encaissement
	var type_encaissement
	int fk_patient
HistoriqueReservations
	int id_reservation
	var CIN
	DateTime date_reservation
	DateTime date_de_fin_reservation
	int id_chambre_vous_convient
	int fk_chambre
	var nom
	var prenom
	var telephone
	var status_reservation
	int nombre_reservation
	DateTime date_reservation
	DateTime date_de_fin_reservation
	TimeStamp date
Menu
	int id_repas
	var nom_repas
	var aperitifs
	var desert
	var categorie
	date jour
	time temps

Admissions
    int id_admission
    int fk_patient
    TimeStamp date
Rendez_vous
    int id_rendez_vous
    var CIN
    DateTime date_rendezvous
    TimeStamp date
Chambre
    int id_chambre
    var nombre_chambre
    var status_chambre
    int prix
    var type_chambre
    int num_lit_vides
    int fk_lit
Lit
    int id_lit
    int nombre
    int fk_chambre
Historique
    int id_historique
    int fk_patient
HistoriqueDossier
    int id_dossier 
    var CIN
    var title_dossier
    var nom_patient
    TimeStamp date
    text chahier_sante
    var pass_vaccinal
    int fk_medecin
    int fk_chambre
    int fk_medicament
    var profession
    var status_dossier
    int fk_rendezvous
HistoriqueRendez_vous
    int id_rendez_vous
    var CIN
    DateTime date_rendezvous
    TimeStamp date
Resrevations
    int id_reservation
    var CIN
    DateTime date_reservation
    DateTime date_fin_reservation
    int fk_chambre
    var nom
    var prenom
    var telephone
    var status_reservation
    int nombre_reservation
    TimeStamp date

Medecin {1..n}--{0..n} Specialite
dossier {1..n}-takes care-{1..n} Medecin
Specialite{1..n}--{1..n}Maladie
dossier{1..n}--{0..n}Maladie
patient {1..n}--{1} dossier




// Product {1..n}-is added to-{0..n} Order
// DiscountCode {01}-applied to-{01} Order
