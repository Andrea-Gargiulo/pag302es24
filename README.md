# pag302es24
esercizio gruppo: Villa Gargiulo Zani D'angiolella
questa è la mia parte
prendo appunti e roba che faccio in stage nei momenti liberi

FORMATTAZIONE:
tipoDiOperazione;descrizione;importo;quantità;opCode
char;String;int;float;int

  public String[] getOperazioniDiTipo(char tipo) {
        LinkedList<String> daRestituire = new LinkedList<>();

        try {
            String line;
            while ((line = reader.readLine()) != null) { // Supponendo che "reader" sia attributo della classe "Terminale"
                String[] operazione = line.split(";"); 

                if (operazione.length > 0 && operazione[0].charAt(0) == tipo) {
                    daRestituire.add(line);
                }
            }
        } catch (IOException e) {
            e.printStackTrace();
        }

        return daRestituire.toArray(new String[daRestituire.size()]);
    }
