# Wazuh Custom Rules and Decoders

Este repositorio contiene reglas y decoders desarrollados para ampliar y mejorar la capacidad de detección y análisis de Wazuh.

## Características del Repositorio

- **Decoders Personalizados**: Decoders adicionales para interpretar logs de aplicaciones y dispositivos que no son soportados de forma nativa por Wazuh.
- **Reglas Personalizadas**: Reglas definidas para detectar eventos y amenazas específicas no cubiertas por las reglas estándar de Wazuh.

## Instalación

Para utilizar las reglas y decoders personalizados de este repositorio, sigue los siguientes pasos:

1. Clona este repositorio en tu servidor Wazuh:
    ```bash
    git clone https://github.com/k0jir0900/wazuh.git
    ```

2. Copia los archivos de reglas al directorio de reglas de Wazuh y configura los permisos:
    ```bash
    cp wazuh/rules/*.xml /var/ossec/etc/rules/
    chmod 660 <ruleName>_rules.xml
    chown wazuh:wazuh <ruleName>_rules.xml
    ```

3. Copia los archivos de decoders al directorio de decoders de Wazuh y configura los permisos:
    ```bash
    cp wazuh/decoders/*.xml /var/ossec/etc/decoders/
    chmod 660 <decodersName>_decoders.xml
    chown wazuh:wazuh <decodersName>_decoders.xml
    ```

4. Reinicia el servicio de Wazuh para aplicar los cambios:
    ```bash
    sudo systemctl restart wazuh-manager
    ```
