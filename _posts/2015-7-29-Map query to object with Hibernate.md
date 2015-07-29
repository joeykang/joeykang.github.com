---
layout: post
title: How to map query to object with Hibernate
---
###C# and .Net
	string Sql = "Select A, B, C from members"; 
	IList sqlResult = NHibernateSession.CreateSQLQuery(Sql).List();
	List<Member> objList = new List<Member>();
	foreach (Object[] ob in sqlResult)
	{
		Member aMember = new Member();
		aMember.ID = ob[0] == null ? new Guid() : (Guid)ob[0];
		aMember.Name = (string)ob[1];
		aMember.Address = (string)ob[2];
		objList.Add(aMember);
	}  





