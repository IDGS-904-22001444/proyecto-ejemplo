pipeline {
    // Agente: Ejecuta el pipeline en cualquier agente disponible
    agent any

    // Define las etapas del pipeline
    stages {
        // Etapa de construcción del pipeline principal
        stage('Build') {
            steps {
                // Muestra un mensaje en la consola
                echo 'Construyendo pipeline principal...'
            }
        }
        // Etapa para llamar al pipeline hijo
        stage('Llamar a pipeline hijo') {
            steps {
                script {
                    // Invoca el job 'pipeline-hijo'
                    // Pasa un parámetro de tipo string llamado 'MENSAJE'
                    build job: 'pipeline-hijo',
                        parameters: [
                            string(name: 'MENSAJE', value: 'Hola desde el principal')
                        ]
                }
            }
        }
    }
}
