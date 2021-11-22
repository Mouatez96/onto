@prefix owl: <http://www.w3.org/2002/07/owl#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix xml: <http://www.w3.org/XML/1998/namespace> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix xsp: <http://www.owl-ontologies.com/2005/08/07/xsp.owl#> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix tennis: <http://sport-tennis.org/Tennis#> .




tennis:athlète a rdfs:Class ;
             rdfs:label "jouer" ;
             
tennis:entraineur a rdfs:Class ;
             rdfs:label "entrainneur" ;
             
tennis:sport a rdfs:Class ;
             rdfs:label "sport" ;

tennis:terrain a rdfs:Class ;
             rdfs:label "terrain" ;

tennis:tournoi a rdfs:Class ;
             rdfs:label "tournoi" ;




tennis:entraine a rdf:Property ;
              rdf:type owl:InverseFunctionalProperty ;
              rdfs:domain tennis:entraineur ;
              rdfs:range tennis:atlhète.


tennis:s'entraine a rdf:Property ;
             rdfs:domain tennis:athlète;

tennis:s'entraine a rdf:Property ;
             rdfs:domain tennis:entraineur;
             
tennis:entraine_a a rdf:Property ;
              rdf:type owl:InverseFunctionalProperty ;
              rdfs:domain tennis:entraineur ;
              rdfs:range tennis:terrain.

tennis:s'entraine_a rdf:Property ;
              rdf:type owl:InverseFunctionalProperty ;
              rdfs:domain tennis:athlète ;
              rdfs:range tennis:terrain.

tennis:participe_a rdf:Property ;
              rdf:type owl:InverseFunctionalProperty ;
              rdfs:domain tennis:athlète ;
              rdfs:range tennis:tournoi.

tennis:soutien rdf:Property ;
              rdf:type owl:InverseFunctionalProperty ;
              rdfs:domain tennis:entraineur ;
              rdfs:range tennis:athlète.
              

tennis:appartient rdf:Property ;
              rdf:type owl:InverseFunctionalProperty ;
              rdfs:domain tennis:tennis ;
              rdfs:range tennis:sport .

tennis:contient rdf:Property ;
              rdf:type owl:InverseFunctionalProperty ;
              rdfs:domain tennis:sport ;
              rdfs:range tennis:tennis .
             
             

             
