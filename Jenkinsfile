canalización {
    agente {
        nodo {
            etiqueta 'maven'
        }
    }
    etapas {
        stage ('Pruebas') {
            pasos {
                sh './mvnw prueba limpia'
            }
        }
        stage ('Paquete') {
            pasos {
                sh '''
                    ./mvnw paquete -DskipTests -Dquarkus.package.type = uber-jar 
                '''
                archiveArtifacts 'destino / *. jar' 
            }
        }
    }
}