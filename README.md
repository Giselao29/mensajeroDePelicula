# mensajeroDePelicula

object roberto{
	var peso=90
	var llamada="no realiza"
	
	method peso(){
		
		return peso
	}
	
	method bicicleta(){
		
		peso=peso+1
		
		return peso
	}
	
	method camion(cantidadAcoplados){
		
		peso=peso+500*cantidadAcoplados
		
		return peso
	}
	
	method llamada(){
		
		return llamada
		
	}
		
}

object neo{
	
	var peso=0
	var credito
	var llamada
	
	method peso(){
		
		return peso
	}
	
	method credito(saldoCredito){
		
		credito=saldoCredito
	}
	
	
	method llamada(){
		
		if(credito=="SI"){llamada="realiza" return llamada} else{llamada="no realiza" return llamada}
	}
	
}

	

object destino{
	
	var viaja
	
	var destino
	
	method brooklyn(mensajero){
		
		if(mensajero.peso()<=1000){viaja= "SI" return viaja}else{ viaja="NO" return viaja}
	}
	
	method matrix(mensajero){
	
		if(mensajero.llamada()=="realiza"){viaja= "SI" return viaja}else{ viaja= "NO" return viaja}
	}
	
	method condicion(){
		
		return viaja
		
	}
	
	method destinoAAlgunLado(mensajero){
		
		if(self.brooklyn(mensajero)=="SI"||self.matrix(mensajero)=="SI"){destino="ALGÚN DESTINO ACEPTADO" return destino } else{destino="NINGÚN DESTINO ACEPTADO"return destino }
	
	}
	
	method confirmacionDeViaje(){
		return destino
	}
}

object paquete{
	var pago
	
	method pago(condicion){
		if(condicion=="SI"){pago="SI"} else{ pago="NO"}
	}
	
	method condicion(){
		return pago
	}
}

object mensajero{
	
	method estaAceptado(){
	if(destino.confirmacionDeViaje()=="ALGÚN DESTINO ACEPTADO" && paquete.condicion()=="SI"){ return "VIAJA por estar en condiciones"} else {return "NO VIAJA"}	
	}
	
}
