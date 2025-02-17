public class Nodo{
    private Tipo info;
    private Nodo link;

    public Nodo (Tipo oggetto){
        info = new Tipo (oggetto);
        link = null;
    }
    public Tipo getInfo(){
        return new Tipo (info);
    }
    public void setLink (Nodo link){
        this.link = link;
    }
    public Nodo getLink(){
        return link;
    }
}  

public class Lista {
    private Nodo head;

    private int elementi;

    public Lista(){
        head = null;
        elementi = 0;
    }
}
public void visitaLista(){
    Nodo p = head;

    while(p != null){
        esamina(p.getInfo());
        p = p.getLink();
    }
}

public void inserisciInTesta (Tipo Info){
    Nodo n = new Nodo (info);

    n.setLink(head);

    head = n;
    elementi ++;
}

public void inserisciInCoda (Tipo Info){
    Nodo p = head; 
    Nodo n = new Nodo(info); 

    if (p == null)
    inserisciInTesta();
    else {
        while (p.getLink () != null) 
        p = p.getLink();

        n.setLink(null);
        p.setLink(n);
        elementi ++;
    }
}

public void inserisciInOrdine (Tipo Info){
    if (head == null)
    inserisciInTesta(info);
    else {
        if (info.isBefore(head.getInfo()))
        inserisciInTesta(info);
        else {
            Nodo p = head;
            Nodo pp = head.getLink();
            Nodo n = new Nodo (info);
            while (pp != null && pp.getInfo().isBefore(info)){
                p = pp;
                pp = pp.getLink();
            }
            if(pp == null)
            inserisciInCoda(info);
            else {
                n.setLink(pp);
                p.setLink(n);
                elementi ++;
            }
        }

    }
}
